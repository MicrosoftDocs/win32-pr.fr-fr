---
description: Utilisé pour configurer les composants CAPICOM.
title: objet Paramètres
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: aaeff4c8b65a68938bfab641aceb68fe4efb6334
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095878"
---
# <a name="settings-object-cryptography"></a>objet Paramètres (chiffrement)

\[l’objet **Paramètres** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section configuration requise.\]

l’objet **Paramètres** est utilisé pour configurer les composants capicom.

## <a name="members"></a>Membres

l’objet **Paramètres** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

l’objet **Paramètres** a ces propriétés.




| Propriété | Type d’accès | Description | 
|----------|-------------|-------------|
| <a href="settings-activedirectorysearchlocation.md"><strong>ActiveDirectorySearchLocation</strong></a><br /> | Lecture/écriture<br /> | Définit ou récupère le Active Directory emplacement de recherche. L’emplacement initial n’est pas spécifié par défaut. Lorsque l’emplacement n’est pas spécifié, la recherche s’effectue dans le catalogue global, puis la recherche est effectuée dans le domaine par défaut. La recherche détermine si l’attribut de certificat de l’utilisateur est publié à cet emplacement.<br /> | 
| <a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a><br /> | Lecture/écriture<br /> | Définit ou récupère une valeur booléenne qui indique si les invites de l’interface utilisateur pour l’identité de l’expéditeur ou du signataire peuvent être utilisées. <br /><blockquote>[!Note]<br />La définition de cette propriété ne désactive pas les avertissements générés avant l’utilisation d’une clé privée à partir d’une application Web.</blockquote><br /> | 




 

## <a name="remarks"></a>Notes

l’objet **Paramètres** peut être créé et il est sécurisé pour les scripts. le ProgID de l’objet **Paramètres** est capicom. Paramètres. 1.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objets de chiffrement**](cryptography-objects.md)
</dt> </dl>

 

 




