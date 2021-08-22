---
description: initialise un objet de service système pour installer un objet ActiveX lorsque l’utilisateur actuel n’est pas autorisé à installer l’objet.
ms.assetid: 42f7cf83-789b-42ea-bb1a-4b79137188ea
title: Interface IeAxiService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService
api_type:
- COM
api_location: ''
ms.openlocfilehash: f799b0b306d10e8246afbef83e4677729f6a735a52e5e4ed4954b873ec5b6201
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119414719"
---
# <a name="ieaxiservice-interface"></a>Interface IeAxiService

l’interface **IAxiService** initialise un objet service système pour installer un objet ActiveX lorsque l’utilisateur actuel n’est pas autorisé à installer l’objet.

La classe [**CIeAxiInstallerService**](cieaxiinstallerservice.md) implémente cette interface.

Cette interface n’est pas déclarée dans un en-tête public. Les applications doivent les définir elles-mêmes. Le fragment IDL (Interface Definition Language) suivant décrit cette interface, y compris son IID.

``` syntax
[
    object,
    uuid(E9E92380-9ECD-4982-A0EB-6815A56CCF27),
    pointer_default(unique)
]

interface IeAxiService : IUnknown{

    
    HRESULT Initialize(
            [in]        HWND            hwndParent,
            [in]        DWORD           dwClientPID,
            [in]        BSTR            bstrDesktop,
            [in]        BSTR            bstrClsID,              
            [in]        BSTR            bstrURL,                
            [out]       BSTR *          pbstrNonce,            
            [out]       IUnknown**      ppISyncBrokerInterface  
            );  
 
    HRESULT Cleanup();
};
```

## <a name="members"></a>Membres

L’interface **IeAxiService** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IeAxiService** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IeAxiService** possède ces méthodes.



| Méthode                                        | Description                                                        |
|:----------------------------------------------|:-------------------------------------------------------------------|
| [**Nettoyage**](ieaxiservice-cleanup.md)       | Libère les ressources utilisées par l’interface **IeAxiService** .<br/> |
| [**Initialiser**](ieaxiservice-initialize.md) | vérifie et télécharge un objet ActiveX.<br/>                 |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows vista Business, Windows vista Enterprise, Windows les applications de bureau vista Ultimate \[ uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiService est défini en tant que E9E92380-9ECD-4982-A0EB-6815A56CCF27<br/>                           |



 

