---
description: Définit ou récupère une valeur booléenne qui spécifie si les invites de l’interface utilisateur pour l’identité de l’expéditeur ou du signataire peuvent être utilisées.
ms.assetid: b9765de4-0b94-4006-aaa8-9ad6858da1f4
title: Paramètres. Propriété EnablePromptForCertificateUI
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings.EnablePromptForCertificateUI
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e494c98e2a828b512b0bb66dc2a44cba8c37792c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095885"
---
# <a name="settingsenablepromptforcertificateui-property"></a>Paramètres. Propriété EnablePromptForCertificateUI

\[La propriété **EnablePromptForCertificateUI** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.\]

La propriété **EnablePromptForCertificateUI** définit ou récupère une valeur booléenne qui spécifie si les invites de l’interface utilisateur pour l’identité de l’expéditeur ou du signataire peuvent être utilisées.

## <a name="syntax"></a>Syntaxe


```VB
Settings.EnablePromptForCertificateUI As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

Si la **valeur est true**, les invites de l’interface utilisateur pour l’identité de l’expéditeur ou du signataire peuvent être utilisées. La valeur par défaut est **false**.

> [!Note]  
> La définition de cette propriété ne désactive pas les avertissements générés avant l’utilisation d’une clé privée à partir d’une application Web.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Paramètres**](settings.md)
</dt> </dl>

 

 




