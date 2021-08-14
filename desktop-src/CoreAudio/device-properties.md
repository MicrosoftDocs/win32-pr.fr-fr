---
description: Propriétés de l’appareil
ms.assetid: ad8753ba-ad20-4122-b0f2-eb165f98db67
title: Propriétés de l’appareil (API audio principales)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47e1a5068329ea2da794b68b777aa989a2e8b4a665df082982916942aa15b56e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118407017"
---
# <a name="device-properties-core-audio-apis"></a>Propriétés de l’appareil (API audio principales)

Pendant le processus d’énumération des [appareils de point de terminaison audio](audio-endpoint-devices.md), une application cliente peut interroger les objets de point de terminaison pour leurs propriétés d’appareil. Les propriétés de l’appareil sont exposées dans l’implémentation de l’interface **IPropertyStore** de l’API MMDevice. À partir d’une référence à l’interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) d’un objet de point de terminaison, un client peut obtenir une référence à la Banque de propriétés de l’objet de point de terminaison en appelant la méthode [**IMMDevice :: OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) .

L’objet de magasin de propriétés expose une interface **IPropertyStore** . Les deux méthodes principales de cette interface sont **IPropertyStore :: GetValue**, qui obtient une valeur de propriété de périphérique, et **IPropertyStore :: SetValue**, qui définit une valeur de propriété d’appareil. pour plus d’informations sur **IPropertyStore**, consultez la documentation SDK Windows.

L’implémentation de l’API MMDevice de la Banque de propriétés est différente de l’objet de magasin de propriétés de Shell standard. Pour modifier une valeur de propriété, l’application cliente doit appeler la méthode **IPropertyStore :: SetValue** . Pendant cet appel, les nouvelles valeurs sont définies et écrites dans le registre. Par conséquent, l’application n’a pas besoin d’appeler la méthode **IPropertyStore :: Commit** après l’appel **SetValue** . Le descripteur du Registre est fermé uniquement lorsque le client libère le pointeur d’interface.

En règle générale, les applications clientes tierces appellent la méthode **GetValue** , mais pas la méthode **SetValue** . Le gestionnaire des points de terminaison définit les propriétés de l’appareil de base pour les points de terminaison. le gestionnaire des points de terminaison est le composant Windows Vista qui est chargé de détecter la présence d’appareils de point de terminaison audio.

Chaque \_ identificateur de propriété de type d’éléments de la liste suivante est une constante de type **PROPERTYKEY** définie dans le fichier d’en-tête Functiondiscoverykeys \_ devpkey. h. Tous les périphériques de point de terminaison audio possèdent ces trois propriétés d’appareil.



| Propriété                                                                         | Description                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Deviceinterface \_ FriendlyName FriendlyName**](pkey-deviceinterface-friendlyname.md) | Nom convivial de la carte audio à laquelle l’appareil de point de terminaison est attaché (par exemple, « carte audio XYZ »). Le membre **PROPVARIANT** **VT** est défini sur VT \_ LPWStr et le membre **pwszVal** pointe sur une chaîne de caractères larges se terminant par un caractère null qui contient le nom convivial. |
| [**Périphérique de l' \_ appareil \_**](pkey-device-devicedesc.md)                       | Description de l’appareil du point de terminaison (par exemple, « Speakers »). Le membre **PROPVARIANT** **VT** est défini sur VT \_ LPWStr et le membre **pwszVal** pointe sur une chaîne de caractères larges se terminant par un caractère null qui contient la description de l’appareil.                                       |
| [**Périphérique de l' \_ appareil \_**](pkey-device-friendlyname.md)                   | Nom convivial de l’appareil de point de terminaison (par exemple, « Speakers (carte audio XYZ) »). Le membre **PROPVARIANT** **VT** est défini sur VT \_ LPWStr et le membre **pwszVal** pointe sur une chaîne de caractères larges se terminant par un caractère null qui contient le nom convivial.                             |



 

Certains périphériques de point de terminaison audio peuvent avoir des propriétés supplémentaires qui n’apparaissent pas dans la liste précédente. Pour plus d’informations sur les propriétés supplémentaires, consultez [Propriétés du point de terminaison audio](audio-endpoint-properties.md). pour plus d’informations sur **PROPERTYKEY**, consultez la documentation SDK Windows.

L’exemple de code suivant imprime les noms complets de tous les appareils de point de terminaison de rendu audio dans le système :


```C++
//-----------------------------------------------------------
// This function enumerates all active (plugged in) audio
// rendering endpoint devices. It prints the friendly name
// and endpoint ID string of each endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);

void PrintEndpointNames()
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDeviceCollection *pCollection = NULL;
    IMMDevice *pEndpoint = NULL;
    IPropertyStore *pProps = NULL;
    LPWSTR pwszID = NULL;

    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->EnumAudioEndpoints(
                        eRender, DEVICE_STATE_ACTIVE,
                        &pCollection);
    EXIT_ON_ERROR(hr)

    UINT  count;
    hr = pCollection->GetCount(&count);
    EXIT_ON_ERROR(hr)

    if (count == 0)
    {
        printf("No endpoints found.\n");
    }

    // Each loop prints the name of an endpoint device.
    for (ULONG i = 0; i < count; i++)
    {
        // Get pointer to endpoint number i.
        hr = pCollection->Item(i, &pEndpoint);
        EXIT_ON_ERROR(hr)

        // Get the endpoint ID string.
        hr = pEndpoint->GetId(&pwszID);
        EXIT_ON_ERROR(hr)
        
        hr = pEndpoint->OpenPropertyStore(
                          STGM_READ, &pProps);
        EXIT_ON_ERROR(hr)

        PROPVARIANT varName;
        // Initialize container for property value.
        PropVariantInit(&varName);

        // Get the endpoint's friendly-name property.
        hr = pProps->GetValue(
                       PKEY_Device_FriendlyName, &varName);
        EXIT_ON_ERROR(hr)

        // Print endpoint friendly name and endpoint ID.
        printf("Endpoint %d: \"%S\" (%S)\n",
               i, varName.pwszVal, pwszID);

        CoTaskMemFree(pwszID);
        pwszID = NULL;
        PropVariantClear(&varName);
        SAFE_RELEASE(pProps)
        SAFE_RELEASE(pEndpoint)
    }
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pCollection)
    return;

Exit:
    printf("Error!\n");
    CoTaskMemFree(pwszID);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pCollection)
    SAFE_RELEASE(pEndpoint)
    SAFE_RELEASE(pProps)
}
```



La macro ayant échoué dans l’exemple de code précédent est définie dans le fichier d’en-tête winerror. h.

Dans l’exemple de code précédent, le corps de la boucle **for** de la fonction PrintEndpointNames appelle la méthode [**IMMDevice :: GetId**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid) pour obtenir la [chaîne d’ID de point de terminaison](endpoint-id-strings.md) pour le périphérique de point de terminaison audio représenté par l’instance d’interface **IMMDevice** . La chaîne identifie de façon unique l’appareil par rapport à tous les autres périphériques de point de terminaison audio dans le système. Un client peut utiliser la chaîne d’ID de point de terminaison pour créer une instance du périphérique de point de terminaison audio ultérieurement ou dans un processus différent en appelant la méthode [**IMMDeviceEnumerator :: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) . Les clients doivent traiter le contenu de la chaîne d’ID de point de terminaison comme opaque. Autrement dit, les clients ne doivent pas tenter d’analyser le contenu de la chaîne pour obtenir des informations sur l’appareil. La raison en est que le format de chaîne n’est pas défini et peut passer d’une implémentation de l’API MMDevice à la suivante.

Les noms d’appareil conviviaux et les chaînes d’ID de point de terminaison obtenus par la fonction PrintEndpointNames dans l’exemple de code précédent sont identiques aux noms de périphérique convivial et aux chaînes d’ID de point de terminaison fournis par DirectSound pendant l’énumération de l’appareil. Pour plus d’informations, consultez [événements audio pour les applications audio héritées](audio-events-for-legacy-audio-applications.md).

Dans l’exemple de code précédent, la fonction PrintEndpointNames appelle la fonction **CoCreateInstance** pour créer un énumérateur pour les périphériques de point de terminaison audio dans le système. À moins que le programme appelant n’appelait auparavant la fonction **CoInitialize** ou **CoInitializeEx** pour initialiser la bibliothèque com, l’appel **CoCreateInstance** échouera. pour plus d’informations sur **CoCreateInstance**, **coinitialize** et **CoInitializeEx**, consultez la documentation SDK Windows.

Pour plus d’informations sur les interfaces **IMMDeviceEnumerator**, **IMMDeviceCollection** et **IMMDevice** , consultez [API MMDevice](mmdevice-api.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Périphériques de point de terminaison audio](audio-endpoint-devices.md)
</dt> </dl>

 

 



