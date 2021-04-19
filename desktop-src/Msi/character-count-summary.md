---
description: La propriété de résumé du nombre de caractères est utilisée uniquement dans les transformations.
ms.assetid: d26d24a5-558e-4333-ae39-ffba1bbc5247
title: Propriété de résumé du nombre de caractères
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afc99c065721f0f0b94691a12e00204305940efd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530530"
---
# <a name="character-count-summary-property"></a>Propriété de résumé du nombre de caractères

La propriété de **Résumé du nombre de caractères** est utilisée uniquement dans les transformations. Cette partie du flux d’informations de résumé est divisée en mots de 2 16 bits. Le mot supérieur contient les [*indicateurs de validation*](t-gly.md)de la transformation. Le mot inférieur contient les [*indicateurs de condition d’erreur de transformation*](t-gly.md).

Cette propriété doit avoir la valeur null dans un package d’installation ou un package de correctifs.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP.<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Descriptions des propriétés de synthèse](summary-property-descriptions.md)
</dt> </dl>

 

 




