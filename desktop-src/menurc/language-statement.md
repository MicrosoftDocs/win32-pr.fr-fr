---
title: LANGUAGE (instruction)
description: Définit la langue de toutes les ressources jusqu’à l’instruction de langage suivante ou jusqu’à la fin du fichier.
ms.assetid: 175e27e2-903a-4aaf-89ef-532166b167e8
keywords:
- Menus de l’instruction de langage et autres ressources
topic_type:
- apiref
api_name:
- LANGUAGE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9563ba2ec00362a3b9caa3911a701919a81cae1e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104507910"
---
# <a name="language-statement"></a>LANGUAGE (instruction)

Définit la langue de toutes les ressources jusqu’à l’instruction de **langage** suivante ou jusqu’à la fin du fichier.

Lorsque l’instruction **Language** apparaît avant le début du corps d’une définition de ressource [**accélérateurs**](accelerators-resource.md), [**DIALOGEX**](dialogex-resource.md), [**menu**](menu-resource.md), [**RCDATA**](rcdata-resource.md)ou [**STRINGTABLE**](stringtable-resource.md) , la langue spécifiée s’applique uniquement à cette ressource.

``` syntax
LANGUAGE language, sublanguage
```

<dl> <dt>

<span id="language"></span><span id="LANGUAGE"></span>*sous*
</dt> <dd>

Identificateur de langue.

</dd> <dt>

<span id="sublanguage"></span><span id="SUBLANGUAGE"></span>*sous-langue*
</dt> <dd>

Identificateur de sous-langue.

</dd> </dl>

Pour plus d’informations, consultez [constantes et chaînes](/windows/desktop/Intl/language-identifier-constants-and-strings)de l’identificateur de langue.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ACCÉLÉRATEURS**](accelerators-resource.md)
</dt> <dt>

[**ATTRIBUTS**](characteristics-statement.md)
</dt> <dt>

[**MENUS**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**Version**](version-statement.md)
</dt> </dl>

 

 