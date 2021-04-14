---
title: Interface IWMDRMDeviceApp2
description: L’interface IWMDRMDeviceApp2 étend IWMDRMDeviceApp en fournissant une nouvelle version de la méthode QueryDeviceStatus.
ms.assetid: a7e28d5a-041f-4102-97db-0c77ca146e26
keywords:
- Interface IWMDRMDeviceApp2 Windows Media Gestionnaire de périphériques
- Interface IWMDRMDeviceApp2 Windows Media Gestionnaire de périphériques, Description
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp2
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df4bfdb023198631b16ffa0e511488fa52423c5e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104313135"
---
# <a name="iwmdrmdeviceapp2-interface"></a>Interface IWMDRMDeviceApp2

L’interface **IWMDRMDeviceApp2** étend [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) en fournissant une nouvelle version de la méthode [**QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) . **QueryDeviceStatus2** permet à l’appelant de demander une exigence DRM spécifique.

Pour accéder à cette interface, appelez **CoCreateInstance** et transmettez le CLSID \_ WMDRMDeviceApp.

> [!Note]  
> Cette interface est définie dans le fichier d’en-tête généré à partir de WMDRMDeviceApp. idl. Cet en-tête **\# comprend** « WMDM. h ». Vous devrez peut-être modifier ce nom de fichier pour qu’il corresponde à l’en-tête généré à partir de WMDM. idl.

 

## <a name="members"></a>Membres

L’interface **IWMDRMDeviceApp2** hérite de [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md). **IWMDRMDeviceApp2** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWMDRMDeviceApp2** possède ces méthodes.



| Méthode                                                            | Description                                                          |
|:------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md) | Interroge un appareil pour obtenir un État ou une fonctionnalité DRM spécifique.<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IWMDRMDeviceApp**](iwmdrmdeviceapp.md)
</dt> <dt>

[**Gestion du contenu protégé dans l’application**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Interfaces pour les applications**](interfaces-for-applications.md)
</dt> <dt>

[**Contrôle de l’utilisation du contenu**](metering-content-usage.md)
</dt> </dl>

 

 





