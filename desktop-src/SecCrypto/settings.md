---
description: Utilisé pour configurer les composants CAPICOM.
title: Settings (objet)
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
ms.openlocfilehash: 27042f9602167f3eb0c1272f7c19fa1170abab40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528883"
---
# <a name="settings-object-cryptography"></a>Objet Settings (Cryptography)

\[L’objet **Settings** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.\]

L’objet **Settings** est utilisé pour configurer les composants CAPICOM.

## <a name="members"></a>Membres

L’objet **Settings** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **Settings** a ces propriétés.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Propriété</th>
<th style="text-align: left;">Type d’accès</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="settings-activedirectorysearchlocation.md"><strong>ActiveDirectorySearchLocation</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Définit ou récupère le Active Directory emplacement de recherche. L’emplacement initial n’est pas spécifié par défaut. Lorsque l’emplacement n’est pas spécifié, la recherche s’effectue dans le catalogue global, puis la recherche est effectuée dans le domaine par défaut. La recherche détermine si l’attribut de certificat de l’utilisateur est publié à cet emplacement.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Définit ou récupère une valeur booléenne qui indique si les invites de l’interface utilisateur pour l’identité de l’expéditeur ou du signataire peuvent être utilisées. <br/>
<blockquote>
[!Note]<br />
La définition de cette propriété ne désactive pas les avertissements générés avant l’utilisation d’une clé privée à partir d’une application Web.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Notes

L’objet **Settings** peut être créé et il est sécurisé pour les scripts. Le ProgID de l’objet **Settings** est CAPICOM. Paramètres. 1.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objets de chiffrement**](cryptography-objects.md)
</dt> </dl>

 

 




