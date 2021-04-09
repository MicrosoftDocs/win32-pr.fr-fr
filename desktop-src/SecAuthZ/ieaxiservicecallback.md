---
description: Appelée par l’interface IeAxiSystemInstaller pour vérifier qu’un objet ActiveX peut être installé.
ms.assetid: d5cd6263-d07e-4261-9463-b9a06e883f16
title: Interface IeAxiServiceCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiServiceCallback
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3ad276126548ac6d5fdc2c828f722c90b43ad679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869025"
---
# <a name="ieaxiservicecallback-interface"></a>Interface IeAxiServiceCallback

L’interface **IeAxiServiceCallback** est appelée par l’interface [**IeAxiSystemInstaller**](ieaxisysteminstaller.md) pour vérifier qu’un objet ActiveX peut être installé.

La classe [**CIeAxiInstallerService**](cieaxiinstallerservice.md) implémente cette interface.

Cette interface n’est pas déclarée dans un en-tête public. Les applications doivent les définir elles-mêmes. Le fragment IDL (Interface Definition Language) suivant décrit cette interface, y compris son IID.

``` syntax
[
    object,
    uuid(1823E7BA-EC36-447a-9B2E-B4912E15AFE7),
    dual,
    nonextensible,
    pointer_default(unique)
]

interface IeAxiServiceCallback : IUnknown
{
    HRESULT VerifyFile(
                       [in] BSTR bstrFileUrl,
                       [out] BSTR * bstrApprovedFileName);
}

```

## <a name="members"></a>Membres

L’interface **IeAxiServiceCallback** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IeAxiServiceCallback** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IeAxiServiceCallback** possède ces méthodes.



| Méthode                                                | Description                                                                                                                                    |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**VerifyFile**](ieaxiservicecallback-verifyfile.md) | Effectue des vérifications de sécurité sur l’objet ActiveX spécifié et retourne l’emplacement où le fichier. cab correspondant a été téléchargé.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista Professionnel, Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiServiceCallback est défini en tant que 1823E7BA-EC36-447A-9B2E-B4912E15AFE7<br/>                   |



 

