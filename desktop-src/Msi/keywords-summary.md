---
description: La propriété Résumé des mots clés dans les bases de données d’installation ou les transformations contient une liste de mots clés.
ms.assetid: e19dc495-e4d4-465f-8464-c60af8985334
title: Propriété Résumé des mots clés
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a572161e440b440010d43f598e2baa453dbca514d71aa6f0f672deb7c726fa2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680309"
---
# <a name="keywords-summary-property"></a>Propriété Résumé des mots clés

La propriété **Résumé des mots clés** dans les bases de données d’installation ou les transformations contient une liste de mots clés. Les mots clés peuvent être utilisés par les explorateurs de fichiers pour effectuer des recherches dans les mots clés d’un fichier. Cette propriété contient la liste des sources du correctif dans un package correctif.

C’est à l’auteur d’une base de données d’installation, d’une transformation ou d’un package de correctifs de fournir la valeur de cette propriété dans les informations de résumé. Les auteurs doivent effectuer les opérations suivantes pour déterminer la valeur correcte.

-   Dans un package d’installation, définissez la valeur de cette propriété sur une liste de mots clés. Le mot clé doit inclure « installer », ainsi que des mots clés spécifiques au produit et peut être localisé.
-   Dans une transformation, définissez la valeur de cette propriété sur une liste de mots clés. Le mot clé doit inclure « installer », ainsi que des mots clés spécifiques au produit et peut être localisé.
-   Dans un package correctif, définissez la valeur de cette propriété sur une liste délimitée par des points-virgules des emplacements réseau ou URL des sources du correctif. Une fois le correctif installé, le programme d’installation les ajoute à la liste source pour le package de correctifs. Si le correctif mis en cache est manquant, le programme d’installation peut rechercher une source à l’emplacement d’origine, un emplacement ajouté à la liste source par la propriété **Résumé des mots clés** ou un emplacement ajouté à la liste source à l’aide des fonctions [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) ou [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Descriptions des propriétés de synthèse](summary-property-descriptions.md)
</dt> </dl>

 

 




