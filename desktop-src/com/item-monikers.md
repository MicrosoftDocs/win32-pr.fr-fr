---
title: Monikers d’élément
description: Une autre classe moniker implémentée par OLE est le moniker d’élément, qui peut être utilisé pour identifier un objet contenu dans un autre objet.
ms.assetid: ddcf3669-4ad0-4a4e-80a6-eb78058cff09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57b692502ba44519a2c51a661ef62a51e133ac04
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293706"
---
# <a name="item-monikers"></a>Monikers d’élément

Une autre classe moniker implémentée par OLE est le *moniker d’élément*, qui peut être utilisé pour identifier un objet contenu dans un autre objet. Un type d’objet contenu est un objet OLE incorporé dans un document composé. Un document composé peut identifier les objets incorporés qu’il contient en affectant chacun un nom arbitraire, tel que « embedobj1 », « embedobj2 », etc. Un autre type d’objet contenu est une sélection d’utilisateur dans un document, telle qu’une plage de cellules dans une feuille de calcul ou une plage de caractères dans un document texte. Un objet qui se compose d’une sélection est appelé *Pseudo-objet* , car il n’est pas traité comme un objet distinct tant qu’un utilisateur n’a pas marqué la sélection. Une feuille de calcul peut identifier une plage de cellules à l’aide d’un nom tel que « 1A : 7F », tandis qu’un document de traitement de texte peut identifier une plage de caractères à l’aide du nom d’un signet.

Un moniker d’élément est surtout utile lorsqu’il est concaténé, ou *composé*, avec un autre moniker, qui identifie le conteneur. Un moniker d’élément est généralement créé, puis composé sur (par exemple) un moniker de fichier pour créer l’équivalent d’un chemin d’accès complet à l’objet. Par exemple, vous pouvez composer le moniker de fichier « c : \\ work \\report.doc » (qui identifie l’objet conteneur) avec le moniker d’élément « embedobj1 » (qui identifie un objet dans le conteneur) pour former le moniker « c : \\ Work \\report.doc\\ embedobj1 », qui identifie de façon unique un objet particulier dans un fichier particulier. Vous pouvez également concaténer des monikers d’élément supplémentaires pour identifier les objets profondément imbriqués. Par exemple, si « embedobj1 » est le nom d’un objet Spreadsheet, pour identifier une certaine plage de cellules dans cet objet Spreadsheet, vous pouvez ajouter un autre moniker d’élément pour créer un moniker qui serait l’équivalent de « c : \\ work \\report.doc\\ Embedobj1 \\ 1a : 7F ».

Lorsqu’il est associé à un moniker de fichier, un moniker d’élément forme un chemin d’accès complet. Les monikers d’élément étendent donc la notion de noms de chemin d’accès au-delà du système de fichiers, en définissant des noms de chemin d’accès pour identifier des objets individuels, pas seulement des fichiers.

Il existe une différence significative entre un moniker d’élément et un moniker de fichier. Le chemin d’accès contenu dans un moniker de fichier est significatif pour toute personne qui comprend le système de fichiers, tandis que le chemin d’accès partiel contenu dans un moniker d’élément est significatif uniquement pour un conteneur particulier. Tout le monde sait ce que « c : \\ work \\report.doc » fait référence, mais un seul objet conteneur particulier sait ce que fait « 1a : 7F ». Un conteneur ne peut pas interpréter un moniker d’élément créé par une autre application ; le seul conteneur qui sait quel objet est référencé par un moniker d’élément est le conteneur qui a affecté le moniker d’élément à l’objet en premier lieu. Pour cette raison, la source de l’objet nommé par la combinaison d’un moniker de fichier et d’élément ne doit pas implémenter [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile), pour faciliter la liaison du moniker de fichier, mais également [**IOleItemContainer**](/windows/desktop/api/OleIdl/nn-oleidl-ioleitemcontainer) pour faciliter la résolution du nom du moniker d’élément dans l’objet approprié, dans le contexte d’un fichier.

L’avantage des monikers est que quelqu’un qui utilise un moniker pour localiser un objet n’a pas besoin de comprendre le nom contenu dans le moniker d’élément, à condition que le moniker d’élément fasse partie d’un composite. En règle générale, il n’est pas judicieux que le moniker d’un élément existe seul. Au lieu de cela, vous composeriez un moniker d’élément sur un moniker de fichier. Vous appelez ensuite [**IMoniker :: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) sur le composite, qui lie les monikers individuels qu’il contient, en interprétant les noms.

Pour créer un objet moniker d’élément et retourner son pointeur vers le fournisseur de monikers, OLE fournit la fonction d’assistance [**CreateItemMoniker**](/windows/desktop/api/Objbase/nf-objbase-createitemmoniker). Cette fonction crée un objet moniker d’élément et retourne son pointeur au fournisseur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Anti-monikers](anti-monikers.md)
</dt> <dt>

[Monikers de classe](class-monikers.md)
</dt> <dt>

[Monikers composites](composite-monikers.md)
</dt> <dt>

[Monikers de fichiers](file-monikers.md)
</dt> <dt>

[Monikers de pointeur](pointer-monikers.md)
</dt> </dl>

 

 




