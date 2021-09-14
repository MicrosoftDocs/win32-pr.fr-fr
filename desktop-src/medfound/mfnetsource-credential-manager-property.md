---
description: Contient un pointeur vers l’interface IMFNetCredentialManager.
ms.assetid: c0826956-9df1-40ec-8ad1-9e0dca34d847
title: MFNETSOURCE_CREDENTIAL_MANAGER, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3447369cedfa5c516e1d7696aae70834c6ce89a5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313833"
---
# <a name="mfnetsource_credential_manager-property"></a>\_Propriété du gestionnaire d’informations d’identification MFNETSOURCE \_

Contient un pointeur vers l’interface [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) . Utilisez cette propriété pour passer l’implémentation de [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) de l’application à la source réseau.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**IUnknown** , pointeur

VT \_ inconnu

**punkVal**



## <a name="remarks"></a>Notes

Le **Gestionnaire des \_ informations \_ d’identification** de constante MFNETSOURCE définit le **GUID** de la clé de propriété. L’identificateur de propriété (PID) est égal à zéro.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Authentification de la source réseau](network-source-authentication.md)
</dt> <dt>

[Mise en réseau dans Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




