---
title: VERSION (instruction)
description: Définit des informations de version sur une ressource qui peut être utilisée par les outils qui lisent et écrivent des fichiers de ressources.
ms.assetid: 3a33cff3-b8b3-43f4-b43a-ff1d1728cdc1
keywords:
- Menus de l’instruction de VERSION et autres ressources
topic_type:
- apiref
api_name:
- VERSION
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302ffcee38b287afff2697b9c5a5241fa406b55c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678541"
---
# <a name="version-statement"></a>VERSION (instruction)

Définit des informations de version sur une ressource qui peut être utilisée par les outils qui lisent et écrivent des fichiers de ressources. La valeur *DWORD* spécifiée s’affiche avec la ressource dans le compilé. Fichier RES. Toutefois, la valeur n’est pas stockée dans le fichier exécutable et n’a pas d’importance pour le système.

L’instruction **version** apparaît avant le début du corps d’une définition de ressource [**accélérateurs**](accelerators-resource.md), [**DIALOGEX**](dialogex-resource.md), [**menu**](menu-resource.md), [**RCDATA**](rcdata-resource.md)ou [**STRINGTABLE**](stringtable-resource.md) . La valeur spécifiée s’applique uniquement à cette ressource.

``` syntax
VERSION dword
```

<dl> <dt>

<span id="dword"></span><span id="DWORD"></span>*grande*
</dt> <dd>

Valeur **DWORD** définie par l’utilisateur.

</dd> </dl>

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ACCÉLÉRATEURS**](accelerators-resource.md)
</dt> <dt>

[**ATTRIBUTS**](characteristics-statement.md)
</dt> <dt>

[**SOUS**](language-statement.md)
</dt> <dt>

[**MENUS**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> </dl>

 

 




