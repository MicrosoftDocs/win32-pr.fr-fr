---
title: Propriété ConnectionOptions. Password (WSManDisp. h)
description: Définit le mot de passe d’un compte local ou d’un compte de domaine sur l’ordinateur distant. Cette propriété détermine le mot de passe pour l’authentification.
ms.assetid: 61ba54b6-7da0-423e-b5b2-c4dd8aacd042
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de propriétés de mot de passe
- propriété Password Windows Remote Management, objet ConnectionOptions
- Windows Remote Management objet ConnectionOptions, propriété de mot de passe
topic_type:
- apiref
api_name:
- ConnectionOptions.Password
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ffc992b5a0560175d6562a16cf4cb3fd6bc4259eb3b712e26708dc713baba14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898989"
---
# <a name="connectionoptionspassword-property"></a>ConnectionOptions. Password, propriété

Définit le mot de passe d’un compte local ou d’un compte de domaine sur l’ordinateur distant. Cette propriété détermine le mot de passe pour l’authentification. Pour plus d’informations, consultez [authentification pour les connexions à distance](authentication-for-remote-connections.md).

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
ConnectionOptions.Password As String
```



## <a name="property-value"></a>Valeur de la propriété

Chaîne qui contient le mot de passe d’un compte local ou d’un compte de domaine sur l’ordinateur distant.

Si aucune valeur n’est fournie et que l’indicateur **WSManFlagCredUsernamePassword** n’est pas défini, le mot de passe du compte qui exécute le script est utilisé.

Si aucune valeur n’est fournie et que l’indicateur **WSManFlagCredUsernamePassword** est défini, le script invite l’utilisateur à entrer le mot de passe (et le nom d’utilisateur, si ce n’est pas fourni). Si un nom d’utilisateur et un mot de passe valides ne sont pas entrés, une erreur d’accès refusé est retournée.

## <a name="remarks"></a>Remarques

N’oubliez pas que vous ne pouvez pas récupérer le mot de passe. Le mot de passe ne peut être défini qu’avec cette propriété.

si vous créez un objet [**ConnectionOptions**](connectionoptions.md) et que vous utilisez un nom d’utilisateur et un mot de passe pour vous connecter à Windows Remote Management, l’indicateur **WSManFlagCredUserNamePassword** doit être défini sur l’appel à [**WSMan. CreateSession**](wsman-createsession.md).

Pour plus d’informations sur la définition des mots de passe, consultez la section Notes dans [**ConnectionOptions**](connectionoptions.md).

## <a name="examples"></a>Exemples

L’exemple de code suivant crée un objet [**ConnectionOptions**](connectionoptions.md) et définit le **mot de passe**.


```VB
' Create a WSMan object. 
Set objWsman = CreateObject( "WSMAN.Automation" )
' Create a ConnectionOptions object
Set objOptions = objWSMan.CreateConnectionOptions
objOptions.Password = "<password>"
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ConnectionOptions**](connectionoptions.md)
</dt> </dl>

 

 





