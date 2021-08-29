---
description: L’interface IScanProfileUI permet aux applications d’afficher une boîte de dialogue afin que les utilisateurs puissent créer, modifier et supprimer des profils de numérisation.
ms.assetid: d0c7edcc-00d8-49b2-a0f7-fe4bbba90bfb
title: Interface IScanProfileUI (Scanprofileui. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileUI
api_type:
- COM
api_location:
- Scanprofileui.h
ms.openlocfilehash: 9afc030c485b1c4a873416c22217ce159601aad5e619f16ff799dcc68d5375e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706339"
---
# <a name="iscanprofileui-interface"></a>Interface IScanProfileUI

L’interface **IScanProfileUI** permet aux applications d’afficher une boîte de dialogue afin que les utilisateurs puissent créer, modifier et supprimer des profils de numérisation.

## <a name="members"></a>Membres

L’interface **IScanProfileUI** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IScanProfileUI** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IScanProfileUI** possède ces méthodes.



| Méthode                                                             | Description                                                                                      |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) | Affiche une boîte de dialogue qui permet aux utilisateurs de créer, de modifier et de supprimer des profils de numérisation.<br/> |



 

## <a name="remarks"></a>Remarques

La boîte de dialogue est modale. l’utilisateur ne peut pas basculer vers la fenêtre parente tant que la boîte de dialogue n’est pas fermée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                        |
| En-tête<br/>                   | <dl> <dt>Scanprofileui. h</dt> </dl>  |
| MIDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Analyser le schéma de profil](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
