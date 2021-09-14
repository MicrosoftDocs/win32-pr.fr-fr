---
description: installe un objet ActiveX.
ms.assetid: 0eb725a9-ceb8-40e5-808d-ac2b286a48b6
title: Interface IeAxiSystemInstaller
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiSystemInstaller
api_type:
- COM
api_location: ''
ms.openlocfilehash: 391088a70aa845cd685511f10e4eb6e809dc7fcf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127096066"
---
# <a name="ieaxisysteminstaller-interface"></a>Interface IeAxiSystemInstaller

l’interface **IeAxiSystemInstaller** installe un objet ActiveX.

Cette interface n’est pas déclarée dans un en-tête public. Les applications doivent les définir elles-mêmes. Le fragment IDL (Interface Definition Language) suivant décrit cette interface, y compris son IID.

``` syntax
[
    object,
    uuid(a50ea6f8-4764-4299-b309-022b2a8b4d8d),
    
]
interface IeAxiSystemInstaller : IUnknown
{
    
    HRESULT InitializeSystemInstaller(  [in] BSTR bstrUrl,
                                  [in] DWORD dwClientPID,
                                  [in] IUnknown* pCallback,
                                  [out] BSTR * pbstrNonce);
}

```

## <a name="members"></a>Membres

L’interface **IeAxiSystemInstaller** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IeAxiSystemInstaller** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IeAxiSystemInstaller** possède ces méthodes.



| Méthode                                                                              | Description                                       |
|:------------------------------------------------------------------------------------|:--------------------------------------------------|
| [**InitializeSystemInstaller**](ieaxisysteminstaller-initializesysteminstaller.md) | installe l’objet ActiveX spécifié.<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows vista Business, Windows vista Enterprise, Windows les applications de bureau vista Ultimate \[ uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiSystemInstaller est défini en tant que a50ea6f8-4764-4299-B309-022b2a8b4d8d<br/>                   |



 

