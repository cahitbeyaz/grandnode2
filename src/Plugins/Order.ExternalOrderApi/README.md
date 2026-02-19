# External Order API for GrandNode

This plugin lets external systems send orders to your GrandNode shop through a simple API.

## What It Does
- Takes orders from external systems via API
- Creates guest customers automatically
- Manages shipping and billing addresses
- Checks if products exist before placing orders
- Gives clear error messages
- Logs everything for troubleshooting

## Setup
1. Put this plugin in your `src/Plugins` folder
2. Build your solution
3. Go to Admin > Plugins > Local plugins
4. Find "External Order API" and click "Install"

## API Usage

### Endpoint
```
POST /api/order
```

### Request Format
Send a JSON request like this:

```json
{
    "page": 0,
    "size": 50,
    "totalPages": 1,
    "totalElements": 1,
    "content": [
        {
            "shipmentAddress": {
                "id": 80844024,
                "firstName": "Trendyol",
                "lastName": "Müşterisi",
                "company": "",
                "address1": "DSM Grup Danışmanlık İletişim ve Satış Tic. A.Ş. Büyükdere Caddesi Noramin İş Merkezi No:237 Kat:B1 ",
                "address2": "",
                "addressLines": {
                    "addressLine1": "xxx",
                    "addressLine2": "xxx"
                },
                "city": " İstanbul ",
                "cityCode": 34,
                "district": "Şişli",
                "districtId": 54,
                "countyId": 0, 
                "countyName": "XXX", 
                "shortAddress": "xxx", 
                "stateName": "xxx", 
                "postalCode": "10D",
                "countryCode": "TR",
                "neighborhoodId": 32126,
                "neighborhood": "Beyazıt Mah",
                "phone": null,
                "fullName": "Trendyol Müşterisi",
                "fullAddress": "DSM Grup Danışmanlık İletişim ve Satış Tic. A.Ş. Büyükdere Caddesi Noramin İş Merkezi No:237 Kat:B1   Şişli  İstanbul "
            },
            "orderNumber": "80869231",
            "grossAmount": 51.98,
            "totalDiscount": 25.99,
            "totalTyDiscount": 0.00, 
            "taxNumber": null,
            "invoiceAddress": {
                "id": 80844023,
                "firstName": "Trendyol",
                "lastName": "Müşterisi",
                "company": "", 
                "address1": "DSM Grup Danışmanlık İletişim ve Satış Tic. A.Ş. Büyükdere Caddesi Noramin İş Merkezi No:237 Kat:B1 ",
                "address2": "", 
                "addressLines": {
                    "addressLine1": "xxx",
                    "addressLine2": "xxx"
                },
                "city": " İstanbul ",
                "district": "Şişli", 
                "districtId": 1234,
                "countyId": 0, 
                "countyName": "XXX", 
                "shortAddress": "xxx", 
                "stateName": "xxx", 
                "postalCode": "", 
                "countryCode": "TR",
                "neighborhoodId": 32126,
                "neighborhood": "Beyazıt Mah",
                "phone": null,
                "fullName": "Trendyol Müşterisi",
                "fullAddress": "DSM Grup Danışmanlık İletişim ve Satış Tic. A.Ş. Büyükdere Caddesi Noramin İş Merkezi No:237 Kat:B1   Şişli  İstanbul",
                "taxOffice": "Company of OMS's Tax Office", 
                "taxNumber": "Company of OMS's Tax Number" 
            },
            "customerFirstName": "Trendyol",
            "customerEmail": "pf+dym24k@trendyolmail.com",
            "customerId": 99993706,
            "customerLastName": "Müşterisi",
            "id": 11650604, 
            "cargoTrackingNumber": 7340447182689,
            "cargoTrackingLink": "https://kargotakip.trendyol.com/?token=",
            "cargoSenderNumber": "733861966410",
            "cargoProviderName": "Trendyol Express Marketplace",
            "lines": [
                {
                    "quantity": 2,
                    "salesCampaignId": 201642,
                    "productSize": " one size",
                    "merchantSku": "merchantSku",
                    "productName": "Kadın Çivit Mavi Geometrik Desenli Kapaklı Clutch sku1234 sku1234, one size",
                    "productCode": 11954798,
                    "productOrigin": "Tr",
                    "merchantId": 201,
                    "amount": 25.99,
                    "discount": 13.00,
                    "tyDiscount": 0.00, 
                    "discountDetails": [
                        {
                            "lineItemPrice": 13.00,
                            "lineItemDiscount": 12.99,
                            "lineItemTyDiscount": 0.00 
                        },
                        {
                            "lineItemPrice": 12.99,
                            "lineItemDiscount": 13.00,
                            "lineItemTyDiscount": 0.00 
                        }
                    ],
                    "fastDeliveryOptions": [
                        {
                            "type": "SameDayShipping"
                        },
                        {
                            "type": "FastDelivery"
                        }
                    ],
                    "currencyCode": "TRY",
                    "productColor": "No Color",
                    "id": 56040534, 
                    "sku": "sku1234",
                    "vatBaseAmount": 8,
                    "barcode": "barcode1234",
                    "orderLineItemStatusName": "ReturnAccepted",
                    "price": 12.99,
                    "productCategoryId": 11111,
                    "laborCost": 11.11
                }
            ],
            "orderDate": 1542801149863,
            "tcIdentityNumber": "99999999999",
            "identityNumber": "0000000000000",
            "currencyCode": "TRY",
            "packageHistories": [
                {
                    "createdDate": 1542790350607,
                    "status": "Created"
                },
                {
                    "createdDate": 1543789070462,
                    "status": "Delivered"
                },
                {
                    "createdDate": 1542872460911,
                    "status": "Picking"
                },
                {
                    "createdDate": 1542953901874,
                    "status": "Shipped"
                }
            ],
            "shipmentPackageStatus": "ReturnAccepted",
            "status": "Shipped",
            "deliveryType": "normal", 
            "timeSlotId": 0,
            "scheduledDeliveryStoreId": "",
            "estimatedDeliveryStartDate": 1614605119000,
            "estimatedDeliveryEndDate": 1615296319000,
            "totalPrice": 469.90,
            "deliveryAddressType": "Shipment",
            "agreedDeliveryDate": 1622549842955, 
            "agreedDeliveryDateExtendible": true, 
            "extendedAgreedDeliveryDate": 1615296319000, 
            "agreedDeliveryExtensionStartDate": 1615296319000, 
            "agreedDeliveryExtensionEndDate": 1615296319000, 
            "invoiceLink": "",
            "fastDelivery": true,
            "fastDeliveryType": "FastDelivery", 
            "originShipmentDate": 1542790350607, 
            "lastModifiedDate": 1641210225935, 
            "commercial": true, 
            "deliveredByService": false, 
            "micro": true, 
            "giftBoxRequested": true, 
            "etgbNo": "243414X001232", 
            "etgbDate": 1705089600000, 
            "3pByTrendyol": false,
            "containsDangerousProduct": true 
        }
    ]
}
```

### Responses

**Success (200 OK)**
```json
{
  "success": true,
  "orderId": "01234567-89ab-cdef-0123-456789abcdef",
  "orderNumber": "GN-12345"
}
```

**Error (400 Bad Request)**
```json
{
  "errors": {
    "Order": [
      "Product with SKU 'INVALID-SKU' was not found"
    ]
  }
}
```

## How It Works

1. We check if all products exist in your store
2. We create or find the customer by email
3. We set up the shipping and billing addresses
4. We create the shopping cart items
5. We place the order using Cash On Delivery payment method
6. We return the order ID and number

## Error Handling

The API uses standard HTTP status codes:
- `200`: Everything went well
- `400`: Something's wrong with your request
- `500`: Something went wrong on our side

All errors are logged in GrandNode's log system.

## Technical Notes

- The default payment method is Cash On Delivery
- You can extend the plugin to support other payment methods
- Operations are logged for troubleshooting

Images of test
<img width="1902" height="958" alt="image" src="https://github.com/user-attachments/assets/c2946b11-52aa-4f87-9bb2-a6ffd881c134" />

<img width="1898" height="962" alt="image" src="https://github.com/user-attachments/assets/e5cf3042-f279-420e-9f14-7ac2e428a82c" />


