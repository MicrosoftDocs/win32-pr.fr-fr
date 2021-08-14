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
ms.openlocfilehash: c324fef5267ce37b42ede66b618b33148d266ac52dd69662a15bbce6094951ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182837"
---
# <a name="syntaxes-for-attributes-in-active-directory-domain-services"></a>Syntaxes pour les attributs dans Active Directory Domain Services

Active Directory Domain Services définir un ensemble de syntaxes d’attributs pour spécifier le type de données contenues dans un attribut. Les syntaxes prédéfinies n’apparaissent pas réellement dans le répertoire et vous ne pouvez pas ajouter de nouvelles syntaxes. Plusieurs méthodes peuvent être utilisées pour identifier la syntaxe d’une classe d’attributs :

-   Les méthodes [**IADs. obten**](/windows/desktop/api/iads/nf-iads-iads-get), [**IADs. GETEX**](/windows/desktop/api/iads/nf-iads-iads-getex), [**IADs. put**](/windows/desktop/api/iads/nf-iads-iads-put)et [**IADs.**](/windows/desktop/api/iads/nf-iads-iads-putex) biais utilisent la structure [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) pour récupérer et définir les valeurs des attributs d’un objet. Le membre **VT** de cette structure est une valeur **VarType** qui identifie le type de données.
-   Les méthodes des interfaces [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) et [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) utilisent une valeur de l’énumération [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) pour spécifier le type de données.
-   Pour spécifier la syntaxe d’une nouvelle classe d’attributs, définissez les attributs [**attributeSyntax**](/windows/desktop/ADSchema/a-attributesyntax) et [**oMSyntax**](/windows/desktop/ADSchema/a-omsyntax) d’un objet [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) . Si la valeur de **oMSyntax** est 127, vous devez également définir l’attribut [**oMObjectClass**](/windows/desktop/ADSchema/a-omobjectclass) . Pour plus d’informations, consultez [choix d’une syntaxe](choosing-a-syntax.md).

Pour obtenir la liste complète des syntaxes fournies par Active Directory Domain Services, y compris les valeurs **VarType** et [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) correspondantes de chaque syntaxe, consultez [syntaxes](/windows/desktop/ADSchema/syntaxes).

 

 