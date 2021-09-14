---
description: La propriété ProductLanguage spécifie le langage que le programme d’installation doit utiliser pour toutes les chaînes de l’interface utilisateur qui ne sont pas créées dans la base de données.
ms.assetid: 5d798825-c70b-4d5a-b88c-a9db40663f6a
title: Propriété ProductLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3199bd2fcef457b40ad98e52f50c595bc424f9a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009765"
---
# <a name="productlanguage-property"></a>Propriété ProductLanguage

La propriété **ProductLanguage** spécifie le langage que le programme d’installation doit utiliser pour toutes les chaînes de l’interface utilisateur qui ne sont pas créées dans la base de données. Cette propriété doit être un identificateur de langue numérique (LANGID). Si une transformation modifie la langue de l’interface utilisateur dans la base de données, elle doit également modifier la valeur de cette propriété pour refléter la nouvelle langue.

Cette propriété est obligatoire.

## <a name="remarks"></a>Notes

La valeur de la propriété **ProductLanguage** doit être l’une des langues listées dans la propriété [**Résumé du modèle**](template-summary.md) .

Lorsque vous créez un package comme indépendant de la langue, affectez la valeur 0 à la propriété **ProductLanguage** et utilisez la police MS Shell Dlg comme style de texte pour toutes les boîtes de dialogue créées. Étant donné que certaines polices ne prennent pas en charge tous les jeux de caractères, en utilisant cette police, vous pouvez vous assurer que le texte s’affiche correctement sur toutes les versions localisées du système d’exploitation.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




