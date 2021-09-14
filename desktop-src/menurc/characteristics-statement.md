---
title: Instruction de caractéristiques
description: Définit des informations sur une ressource qui peut être utilisée par les outils qui lisent et écrivent les fichiers de définition de ressource.
ms.assetid: 07834b02-a36e-40cc-8907-bff6631842f3
keywords:
- Menus de l’instruction caractéristiques et autres ressources
topic_type:
- apiref
api_name:
- CHARACTERISTICS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de681785fa2ec815b1edbdda913dd8032f8feb8e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293454"
---
# <a name="characteristics-statement"></a>Instruction de caractéristiques

Définit des informations sur une ressource qui peut être utilisée par les outils qui lisent et écrivent les fichiers de définition de ressource. La valeur **DWORD** spécifiée s’affiche avec la ressource dans le fichier. res compilé. Toutefois, la valeur n’est pas stockée dans le fichier exécutable et n’a pas d’importance pour le système.

L’instruction **Characteristics** s’affiche avant le début du corps d’une définition de ressource [**accélérateurs**](accelerators-resource.md), [**boîte de dialogue**](dialog-resource.md), [**menu**](menu-resource.md), [**RCDATA**](rcdata-resource.md)ou [**STRINGTABLE**](stringtable-resource.md) . La valeur spécifiée s’applique uniquement à cette ressource.

``` syntax
CHARACTERISTICS dword
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

[**DIALOGUE**](dialog-resource.md)
</dt> <dt>

[**SOUS**](language-statement.md)
</dt> <dt>

[**MENUS**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> </dl>

 

 




