---
title: Références (ADSI)
description: Les références se produisent lorsque le serveur que vous interrogez ne contient pas ces données, mais peut le trouver.
ms.assetid: 2068ce7a-0b94-4d25-a18f-97f26863bd1d
ms.tgt_platform: multiple
keywords:
- Références (ADSI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d5fb6ad299c2f47efa9723857b53cf7eee5350589757153eaaae869b2c37e6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119444019"
---
# <a name="referrals-adsi"></a>Références (ADSI)

Les références se produisent lorsque le serveur que vous interrogez ne contient pas ces données, mais peut le trouver. Le serveur cible retourne le jeu de résultats, qui peut inclure à la fois les données réelles et une référence à un autre serveur pour récupérer les données supplémentaires. En activant le *repérage de références*, le code client ADSI sous-jacent utilise ces données de référence pour tenter de récupérer l’objet cible à partir du serveur décrit dans les données de référence. Sachez que la désactivation du repérage de références peut aboutir à un jeu de résultats plus petit, tandis que l’activation du repérage de références peut entraîner l’étendue d’une requête sur plusieurs serveurs. Dans la mesure du possible, la solution recommandée consiste à utiliser le catalogue global.

Pour plus d’informations sur les références et le repérage de références dans Active Directory, consultez [références](/windows/desktop/AD/referrals).

Par exemple, lorsqu’un client demande au serveur A (A) d’interroger un objet utilisateur (U), un peut suggérer que le client continue la recherche sur le serveur B (B) si U ne réside pas sur un, mais qu’il est connu sur B. Le client a le choix de poursuivre la référence ou non. Les références de recherche libèrent le client de la nécessité d’une reconnaissance avancée de la capacité de chaque serveur. Toutefois, le client doit spécifier le type de références qu’un serveur doit effectuer.

Active Directory propose des services de référence de recherche. Un client peut choisir l’un des types suivants de repérage de références :

-   Jamais : le serveur ne doit pas générer de référence à un client, même s’il reconnaît qu’un autre serveur stocke les données demandées.
-   External : le serveur doit générer des références si la requête peut être résolue sur un autre serveur d’une arborescence de répertoires différente. Par exemple, un client interroge « OU = Sales, DC = fabrikam, DC = COM » sur le serveur « fab01 » sur le domaine « Fabrikam.com ». Toutefois, l’objet n’appartient pas à « fab01 », mais il est connu pour se trouver sur le serveur « arc01 » sur le domaine « Fabrikam.com ». Par conséquent, « fab01 » fait référence au client à « arc01 ».
-   Subordonné : le serveur doit générer des références si la requête peut être résolue sur un serveur dont le nom constitue un chemin d’accès contigu à partir du serveur d’origine. L’étendue de recherche doit être au niveau de la sous-arborescence.

    Par exemple, le serveur A contient des objets dans « DC = Sales, DC = fabrikam, DC = com ». Le serveur B contient des objets dans « DC = Seattle, DC = Sales, DC = fabrikam, DC = com ». Sachez que le nom du serveur B forme un chemin d’accès contigu à partir du serveur A. Lorsqu’un client contacte le serveur A, demande une recherche de sous-arborescence sur « DC = Sales, DC = fabrikam, DC = com » et spécifie que la référence est un type subordonné, l’événement suivant se produit :

    -   Le serveur A retourne tous les objets qu’il connaît dans son étendue.
    -   Le serveur A informe le client que les objets de « DC = Seattle, DC = Sales, DC = fabrikam, DC = COM » se trouvent sur le serveur B.

    Le client peut choisir de contacter le serveur B. Si c’est le cas, l’événement suivant se produit :

    -   Le serveur B répond avec les objets demandés.
    -   Si le serveur B détecte d’autres serveurs sur le chemin d’accès de nommage contigu et que le processus se poursuit.

-   Toujours : le serveur génère des références si la recherche peut être résolue en fonction du type externe ou du type subordonné.

> [!Note]  
> Dans Active Directory, le catalogue global contient tous les objets d’une entreprise donnée. La recherche d’un serveur de catalogue global donne de meilleures performances que la poursuite des références d’un serveur à un autre.

 

Dans la plupart des cas, le repérage de références est transparent pour l’appelant. Si la référence est un objet d’un domaine ou d’une forêt différent, l’API LDAP sous-jacente tente d’utiliser les informations d’identification actuelles pour établir une liaison à la cible de la référence. Si cette opération réussit, le repérage de références est transparent. En cas d’échec, la référence et un code d’erreur de référence sont renvoyés.

Pour plus d’informations sur l’utilisation des options de repérage de références avec une interface de recherche spécifique, consultez :

-   [Repérage de références avec IDirectorySearch](referral-chasing-with-idirectorysearch.md)
-   [recherche avec ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
-   [Recherche avec OLE DB](searching-with-ole-db.md)

 

 