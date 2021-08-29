---
title: Négociation Media-Type
description: De nombreux protocoles Internet de la couche application sont basés sur l’échange de messages dans un format simple et flexible appelé MIME (Multipurpose Internet Mail Extensions).
ms.assetid: 7a2c9d8f-639a-4865-a62b-63330175f5f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8d9e2694d7df89eeeef8c0a3e7217a88c3bac27da3e68c38aae2ceae24fa56f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130191"
---
# <a name="media-type-negotiation"></a>Négociation Media-Type

De nombreux protocoles Internet de la couche application sont basés sur l’échange de messages dans un format simple et flexible appelé MIME (Multipurpose Internet Mail Extensions). Bien que MIME soit un standard pour l’échange de messages électroniques, il est utilisé aujourd’hui par un large éventail d’applications pour spécifier des formats de données mutuellement comprises comme des types MIME (ou médias). Le processus est appelé *négociation de type de média*.

Les types de média sont des chaînes simples qui désignent un type et un sous-type (par exemple, « text/plain » ou « Text/HTML »). Ils permettent d’étiqueter des données ou de qualifier une demande. Un navigateur Web, par exemple, dans le cadre d’une requête-pour-données HTTP ou d’une requête-pour-informations, spécifie qu’il demande les types de média « image/GIF » ou « image/JPEG », sur lesquels un serveur Web répond en renvoyant le type de média approprié et, si l’appel était une requête-pour les données, dans le format demandé

La négociation de type de média est souvent similaire à la façon dont les applications de bureau existantes négocient avec le presse-papiers du système pour déterminer le format de données à coller lorsqu’un utilisateur choisit modifier/coller ou des requêtes pour les formats lors de la réception d’un pointeur [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) pendant une opération de glisser-déplacer. La principale différence dans la négociation de type de média HTTP est que le client n’a pas connaissance à l’avance des formats disponibles pour le serveur. Par conséquent, le client spécifie les types de médias qu’il prend en charge, dans l’ordre de la plus grande fidélité, et le serveur répond avec le meilleur format disponible.

Les monikers d’URL prennent en charge la négociation de type de média comme un moyen pour les clients et les serveurs Internet de s’accorder sur les formats à utiliser lors du téléchargement de données dans des opérations [**BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) . Pour prendre en charge la négociation de type de média, un client implémente l’interface [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) et appelle la fonction [**RegisterFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775116(v=vs.85)) pour l’inscrire auprès du contexte de liaison. L’énumérateur format répertorie les formats que le client peut accepter. Un moniker d’URL convertit ces formats en types de média lors de la liaison à des URL HTTP.

Les types de média possibles demandés par le client sont représentés aux monikers d’URL via les structures [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) disponibles à partir de l’énumérateur [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) inscrit par l’appelant sur le contexte de liaison : chaque **FORMATETC** spécifie un format de presse-papiers identifiant le type de média. Par exemple, le fragment de code suivant spécifie que le type de média est PostScript.

``` syntax
FORMATETC fmtetc;
fmtetc.cfFormat = RegisterClipboardFormat(CF_MIME_POSTSCRIPT);
. . .
```

Un client peut définir le format du presse-papiers sur le type de support spécial CF \_ null pour indiquer que le type de média par défaut de la ressource vers laquelle pointe l’URL doit être récupéré. Ce format est généralement le dernier qui est intéressé par le client. Quand aucun énumérateur n’est inscrit avec le contexte de liaison, un moniker d’URL fonctionne comme si un énumérateur contenant un [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) unique avec **cfFormat**= CF \_ null est disponible, en téléchargeant automatiquement le type de média par défaut.

Quel que soit le type de support à utiliser, le client est informé du choix au moyen de l’argument *pFormatetc* sur sa méthode [**IBindStatusCallback :: ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) . Le rappel se produit dans le contexte de l’appel du client à [**BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage).

> [!Note]  
> Si le contenu reçu est d’un type de média non reconnu, le client appelle automatiquement [**RegisterMediaTypes**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775118(v=vs.85)) pour inscrire le nouveau type.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Monikers d’URL](url-monikers.md)
</dt> </dl>

 

 