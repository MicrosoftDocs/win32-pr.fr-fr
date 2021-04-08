---
title: Opérations d’Access Control et d’écriture
description: Les modifications de propriété échouent si l’appelant ne dispose pas de droits suffisants.
ms.assetid: eb5b97fb-4654-444e-9f5a-9a4be27ef1a3
ms.tgt_platform: multiple
keywords:
- Opérations de Access Control et d’écriture AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0b8ecab475cd5696a98c985f92ccc24b1dd6072
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842010"
---
# <a name="access-control-and-write-operations"></a>Opérations d’Access Control et d’écriture

Les modifications de propriété échouent si l’appelant ne dispose pas de droits suffisants. Pour les opérations d’écriture effectuées par lot sur plusieurs propriétés, la totalité de l’opération échoue si l’appelant n’a pas les droits nécessaires sur une seule des propriétés modifiées. Par exemple, vous pouvez effectuer plusieurs [**IAD : les appels :P ut**](/windows/desktop/api/iads/nf-iads-iads-put) pour définir plusieurs propriétés sur un objet. Toutefois, lorsque vous appelez [**IADs :: setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) pour écrire les nouvelles données du cache local dans le répertoire, **setinfo** échoue si l’appelant ne dispose pas d’un accès en écriture à toutes les propriétés modifiées. De même, la méthode [**IDirectoryObject :: SetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes) ne peut définir aucune propriété si l’appelant n’a pas accès à toutes les propriétés définies. Par conséquent, vous devez regrouper plusieurs opérations de modification uniquement si vous savez que toutes les modifications ont été effectuées. Pour déterminer les attributs d’un objet d’annuaire que l’appelant a la possibilité de modifier, lisez l’attribut **allowedAttributesEffective** de l’objet.

Si l’appelant ne dispose pas des droits suffisants pour modifier une propriété, les codes de retour suivants peuvent être retournés :

\_propriété e ADS \_ non définie sur la \_ \_ \_ \_ propriété ADS \_ non \_ modifiée

 

 