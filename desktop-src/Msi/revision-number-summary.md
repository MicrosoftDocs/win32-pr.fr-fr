---
description: Pour un package d’installation, la propriété Résumé du numéro de révision contient le code du package du programme d’installation.
ms.assetid: 79702b44-846a-4672-8e22-9b6e3f4b4678
title: Propriété Résumé du numéro de révision
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e97df1eafec2d543be0f975b9f5daca7728267b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541718"
---
# <a name="revision-number-summary-property"></a>Propriété Résumé du numéro de révision

Pour un package d’installation, la propriété **Résumé du numéro de révision** contient le [*code*](p-gly.md) du package du programme d’installation. Pour plus d’informations sur les codes de package, consultez [codes de package](package-codes.md).

Pour une transformation, la propriété **Résumé du numéro de révision** répertorie les GUID et la version des codes de produit des nouveaux produits et originaux et le GUID du code de mise à niveau. La liste est séparée par des points-virgules, comme suit.

«Original-version du produit original-version du produit ; New-Product code New-Product-version ; Upgrade-code»

Pour un package de correctifs, la propriété **Résumé du numéro de révision** spécifie le code correctif du GUID pour le correctif. Elle peut être suivie d’une liste de GUID de code correctif pour les correctifs obsolètes à supprimer lorsque ce correctif est appliqué. Les codes de correctif sont concaténés, sans délimiteur, en séparant les GUID dans la liste.

* * Windows Installer 3,0 : * * si des informations de séquencement sont présentes dans la [table MsiPatchSequence](msipatchsequence-table.md), Windows Installer 3,0 utilise les informations de séquencement dans le tableau et ignore la liste des correctifs obsolètes inclus dans la propriété **Résumé du numéro de révision** . Windows Installer 3,0 peuvent toujours utiliser les informations sur les correctifs obsolètes dans la propriété **Résumé du numéro de révision** si le package ne contient pas de table MsiPatchSequence.

* * Windows Installer 2,0 : * * la [table MsiPatchSequence](msipatchsequence-table.md) n’est pas prise en charge. Windows Installer 2,0 peuvent toujours utiliser les informations sur les correctifs obsolètes dans la propriété **Résumé du numéro de révision** si le package ne contient pas de table MsiPatchSequence.

Cette propriété de résumé est obligatoire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Descriptions des propriétés de synthèse](summary-property-descriptions.md)
</dt> </dl>

 

 




