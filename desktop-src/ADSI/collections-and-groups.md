---
title: Collections et groupes
description: ADSI utilise des objets de collection pour représenter tout ensemble arbitraire d’éléments dans un service d’annuaire qui peut être représenté à l’aide du même type de données.
ms.assetid: 03257cc9-f354-4e1c-8880-936a7acac3ef
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, utilisation de, collections et groupes
- ADSI de collections
- groupes ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9f0f4d699d8dde0c3d70c7449dfe146212b2b30
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103941351"
---
# <a name="collections-and-groups"></a>Collections et groupes

ADSI utilise des objets de collection pour représenter tout ensemble arbitraire d’éléments dans un service d’annuaire qui peut être représenté à l’aide du même type de données. Les objets de collection sont définis sous la forme d’un ensemble de valeurs **Variant** , représentant l’un des types de données Automation valides. Les objets de collection peuvent représenter des informations persistantes telles que les listes de contrôle d’accès et les informations volatiles telles que les travaux d’impression dans une file d’attente à l’impression.

La Convention COM standard pour répertorier le contenu d’un objet collection (ou conteneur) consiste à créer un objet énumérateur qui prend en charge [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), qui a des méthodes pour parcourir la liste d’objets de collection. Les interfaces dans ADSI qui fournissent la méthode d’extraction de la méthode **\_ \_ NewEnum** (Notez les deux traits de soulignement) sont [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) et [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection). ADSI fournit également les fonctions d’assistance [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) et [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) pour les programmes C et C++ afin de simplifier l’énumération. Les clients Automation utilisent implicitement l’énumération lorsqu’ils appellent **Next** dans une boucle **for** .

Les groupes sont simplement des collections d’objets prenant en charge l’interface [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) .

 

 