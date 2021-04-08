---
title: Syntaxes pour les attributs dans Active Directory Domain Services
description: Active Directory Domain Services définir un ensemble de syntaxes d’attributs pour spécifier le type de données contenues dans un attribut.
ms.assetid: 79d27d47-5d03-4ad6-bf97-c387c34fa454
ms.tgt_platform: multiple
keywords:
- Syntaxes pour les attributs de Active Directory Domain Services Active Directory
- Attributs Active Directory, syntaxes pour
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04386e1b4981a81585fe208afa4cca6ed02d4c3c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101413"
---
# <a name="syntaxes-for-attributes-in-active-directory-domain-services"></a>Syntaxes pour les attributs dans Active Directory Domain Services

Active Directory Domain Services définir un ensemble de syntaxes d’attributs pour spécifier le type de données contenues dans un attribut. Les syntaxes prédéfinies n’apparaissent pas réellement dans le répertoire et vous ne pouvez pas ajouter de nouvelles syntaxes. Plusieurs méthodes peuvent être utilisées pour identifier la syntaxe d’une classe d’attributs :

-   Les méthodes [**IADs. obten**](/windows/desktop/api/iads/nf-iads-iads-get), [**IADs. GETEX**](/windows/desktop/api/iads/nf-iads-iads-getex), [**IADs. put**](/windows/desktop/api/iads/nf-iads-iads-put)et [**IADs.**](/windows/desktop/api/iads/nf-iads-iads-putex) biais utilisent la structure [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) pour récupérer et définir les valeurs des attributs d’un objet. Le membre **VT** de cette structure est une valeur **VarType** qui identifie le type de données.
-   Les méthodes des interfaces [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) et [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) utilisent une valeur de l’énumération [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) pour spécifier le type de données.
-   Pour spécifier la syntaxe d’une nouvelle classe d’attributs, définissez les attributs [**attributeSyntax**](/windows/desktop/ADSchema/a-attributesyntax) et [**oMSyntax**](/windows/desktop/ADSchema/a-omsyntax) d’un objet [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) . Si la valeur de **oMSyntax** est 127, vous devez également définir l’attribut [**oMObjectClass**](/windows/desktop/ADSchema/a-omobjectclass) . Pour plus d’informations, consultez [choix d’une syntaxe](choosing-a-syntax.md).

Pour obtenir la liste complète des syntaxes fournies par Active Directory Domain Services, y compris les valeurs **VarType** et [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) correspondantes de chaque syntaxe, consultez [syntaxes](/windows/desktop/ADSchema/syntaxes).

 

 