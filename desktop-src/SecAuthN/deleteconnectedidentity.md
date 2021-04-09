---
description: Supprime les informations d’identification de l’utilisateur utilisées pour l’identité connectée.
ms.assetid: EB32832D-9A8C-4CEB-897A-7E9D24FF84DD
title: DeleteConnectedIdentity, fonction (Indentitystore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteConnectedIdentity
api_type:
- HeaderDef
api_location:
- Indentitystore.h
ms.openlocfilehash: 8079985f916e996a56b4203ad6ad065c1b7664e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033862"
---
# <a name="deleteconnectedidentity-function"></a>DeleteConnectedIdentity fonction)

Supprime les informations d’identification de l’utilisateur utilisées pour l’identité connectée.

## <a name="syntax"></a>Syntaxe


```C++
SEC_ENTRY DeleteConnectedIdentity(
  _In_     PVOID  ProviderHandle,
  _In_opt_ HANDLE UserToken,
  _In_     PSID   UserSid,
  _In_     PWSTR  IdentityUserName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ProviderHandle* \[ dans\]
</dt> <dd>

Descripteur de fournisseur d’identité.

</dd> <dt>

*UserToken* \[ dans, facultatif\]
</dt> <dd>

Jeton de l’utilisateur connecté dont le compte va être converti en compte local. Si *userToken* n’a pas la **valeur null**, le fournisseur d’identité utilise ce jeton pour charger le profil utilisateur et nettoyer les États connectés. Si *userToken* a la **valeur null**, LSA force la déconnexion. Le fournisseur d’identité doit nettoyer tous les États connectés globaux sur cet utilisateur, mais il n’est pas nécessaire que le fournisseur nettoie les États connectés dans le profil utilisateur.

</dd> <dt>

*UserSid* \[ dans\]
</dt> <dd>

SID principal de l’utilisateur connecté. Si *userToken* n’a pas la **valeur null**, ce paramètre est le SID de l’utilisateur du jeton. Si *userToken* a la **valeur null**, ce paramètre est utilisé pour identifier l’utilisateur connecté et nettoyer les États connectés globaux de cet utilisateur.

</dd> <dt>

*IdentityUserName* \[ dans\]
</dt> <dd>

Nom d’utilisateur de l’identité.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction s’exécute correctement, la fonction retourne SEC \_ E \_ OK.

Si la fonction échoue, la fonction peut retourner l’un des codes d’erreur suivants.



| Valeur retournée                                                                                               | Description                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>paramètre d’état \_ non valide \_</dt> </dl>      | Un paramètre n'est pas valide.<br/>                                                                                                                        |
| <dl> <dt>ÉTAT \_ non de \_ ce type d' \_ utilisateur</dt> </dl>          | L’utilisateur identifié par *UserSid* n’existe pas, n’est pas connecté actuellement, ou il n’existe aucune identité dont le nom d’utilisateur correspond à *IdentityUserName*.<br/> |
| <dl> <dt>ressources dont l’État est \_ insuffisant \_</dt> </dl> | La mémoire est insuffisante pour traiter la demande.<br/>                                                                                               |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                  |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                        |
| En-tête<br/>                   | <dl> <dt>Indentitystore. h</dt> </dl> |



 

 




