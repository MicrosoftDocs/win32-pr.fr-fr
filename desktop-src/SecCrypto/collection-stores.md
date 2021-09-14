---
description: À mesure que le nombre de certificats, les listes de révocation de certificats (CRL) et la liste de certificats de confiance (CTL) du regroupement d’un utilisateur se développent, l’organisation de ces certificats devient un problème.
ms.assetid: 13e7e077-e8be-4ba4-99e1-08421fd2452e
title: Magasins de collection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bfeb8ef071d7a5ccf6bc7ce43ba418117879536
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237672"
---
# <a name="collection-stores"></a>Magasins de collection

À mesure que le nombre de [*certificats*](../secgloss/c-gly.md), les [*listes de révocation*](../secgloss/c-gly.md) de certificats (CRL) et la liste de certificats de [*confiance*](../secgloss/c-gly.md) (CTL) du regroupement d’un utilisateur se développent, l’organisation de ces certificats devient un problème. Une solution possible consiste à créer des magasins de certificats distincts pour conserver différents genres de certificats. Cette solution crée un nouveau problème, car une application peut avoir besoin de rechercher dans plusieurs magasins différents pour trouver un certificat spécifique. L’utilisation des magasins logiques ou de collections résout ce problème.

Un magasin [*logique*](../secgloss/l-gly.md) et un magasin de certificats de collection sont des groupes de magasins physiques qui s’affichent dans une application sous la forme d’un magasin unique. Tous les magasins membres d’un magasin logique ou d’un magasin de collections peuvent être recherchés ou énumérés avec un appel de fonction unique pour [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) ou [**CertEnumCertificatesInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore).

L’utilisation de stockages logiques ou de collections offre également une flexibilité difficile à atteindre avec les enregistrements papier. Un certificat dans un seul magasin physique doit peut-être être membre de plusieurs groupes logiques différents. Par conséquent, un magasin physique individuel peut être membre de plusieurs magasins logiques ou de collection, comme indiqué dans l’illustration suivante.

![magasins de collection](images/mancert.png)

Cette illustration présente les concepts de base du magasin de certificats logiques suivants :

-   Un magasin de certificats de collection a un pointeur vers le premier bloc pointeur pour ce magasin de collection.
-   Chaque bloc pointeur d’un magasin de collections a un pointeur vers un magasin frère et un pointeur vers le bloc pointeur suivant de la collection.
-   Chaque magasin frère dans une collection est un magasin de certificats physiques simple.
-   Un magasin de certificats simple peut être un magasin frère de membre dans de nombreux magasins de collection différents.
-   Les certificats ajoutés à un magasin de collections sont ajoutés physiquement à l’un des magasins frères dans la collection.
-   Les certificats d’un magasin frère sont accessibles par n’importe quel magasin de collections dans lequel le magasin frère est membre.

Les magasins de collection sont générés dans une application en ouvrant un magasin de collection à l’aide de [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) , puis en utilisant [**CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection) pour ajouter un magasin frère ouvert au magasin de collections. Un magasin frère peut être supprimé d’un magasin de collection en appelant [**CertRemoveStoreFromCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certremovestorefromcollection).

 

 
