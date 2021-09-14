---
description: 'L’interface IWpdSerializer est utilisée par le pilote de périphérique pour sérialiser les interfaces IPortableDeviceValues vers et depuis les mémoires tampons de données brutes utilisées pour communiquer avec l’application. Les applications n’ont pas besoin d’utiliser cette interface, car les données sont sérialisées et désérialisées automatiquement lors de l’appel de IPortableDevice :: SendCommand. pour accéder à cette interface, appelez CoCreateInstance et Pass dans IID \_ IWpdSerializer.'
ms.assetid: 837bd850-6e27-4f8e-a612-d16f61b92b1d
title: Interface IWpdSerializer (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: dde4bfeea596ccc2691323d484f5583d55ade621
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234462"
---
# <a name="iwpdserializer-interface"></a>Interface IWpdSerializer

L’interface **IWpdSerializer** est utilisée par le pilote de périphérique pour sérialiser les interfaces [**IPortableDeviceValues**](iportabledevicevalues.md) vers et depuis les mémoires tampons de données brutes utilisées pour communiquer avec l’application.

Les applications n’ont pas besoin d’utiliser cette interface, car les données sont sérialisées et désérialisées automatiquement lors de l’appel de [**IPortableDevice :: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

Pour accéder à cette interface, appelez **CoCreateInstance** et Pass dans **IID \_ IWpdSerializer**.

## <a name="members"></a>Membres

L’interface **IWpdSerializer** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWpdSerializer** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWpdSerializer** possède ces méthodes.



| Méthode                                                                                          | Description                                                                                                      |
|:------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**GetBufferFromIPortableDeviceValues**](iwpdserializer-getbufferfromiportabledevicevalues.md) | Sérialise une interface **IPortableDeviceValues** soumise à un tableau d’octets alloué.<br/>                |
| [**GetIPortableDeviceValuesFromBuffer**](iwpdserializer-getiportabledevicevaluesfrombuffer.md) | Désérialise un tableau d’octets en une interface **IPortableDeviceValues** .<br/>                                  |
| [**GetSerializedSize**](iwpdserializer-getserializedsize.md)                                   | Calcule la taille de la mémoire tampon requise pour contenir une interface **IPortableDeviceValues** sérialisée.<br/> |
| [**WriteIPortableDeviceValuesToBuffer**](iwpdserializer-writeiportabledevicevaluestobuffer.md) | Sérialise une interface **IPortableDeviceValues** dans un tableau d’octets alloué par l’appelant.<br/>                   |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces du pilote**](driver-interfaces.md)
</dt> </dl>

 

