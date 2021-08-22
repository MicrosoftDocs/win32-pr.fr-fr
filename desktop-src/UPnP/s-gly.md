---
title: S (API UPnP)
description: Contient les termes relatifs à UPnP qui commencent par la lettre S.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 94be0f7f-8263-40ad-9d48-35540eaa3a3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 459bc1eff834e9bdb4c08b7d372d052faea78f98acc196b21ed7cfd1a2c73abd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999509"
---
# <a name="s-upnp-apis"></a>S (API UPnP)

Contient les termes relatifs à UPnP qui commencent par la lettre S.

[A](a-gly.md) B [C](c-gly.md) [D](d-gly.md) [e](e-gly.md) F G [H](h-gly.md) I J K L M [N](n-gly.md) O [P](p-gly.md) Q [R](r-gly.md) S T [U](u-gly.md) V W X Y Z

<dl> <dt>

<span id="upnp.s_1_gly"></span><span id="UPNP.S_1_GLY"></span>**services**
</dt> <dd>

Un service est une unité fonctionnelle logique. Les services exposent des actions et modélisent tout ou partie des États d’un appareil physique à l’aide de variables d’État.

</dd> <dt>

<span id="upnp.s_2_gly"></span><span id="UPNP.S_2_GLY"></span>**Description du service**
</dt> <dd>

Une description de service est une liste des actions fournies par un service, ainsi que les variables d’état associées aux actions.

</dd> <dt>

<span id="upnp.s_3_gly"></span><span id="UPNP.S_3_GLY"></span>**objet de service**
</dt> <dd>

Un objet de service est la représentation de l’API du point de contrôle d’un service. Un objet de service implémente l’interface [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) .

</dd> <dt>

<span id="upnp.s_4_gly"></span><span id="UPNP.S_4_GLY"></span>**type de service**
</dt> <dd>

Un type de service est un URN qui identifie un service. Il existe une relation un-à-un entre un modèle de service UPnP et un type de service. Plusieurs types de service standard sont définis par les comités de travail du Forum UPnP. Les types de service se présentent sous la forme urn : schemas-UPnP-org : service : serviceType : version. Par exemple, un type de service de scanneur peut être urn : schemas-UPnP-org : service : scanner : 1.

Les fournisseurs UPnP peuvent spécifier des services supplémentaires. Ces services sont dénotés par urn : Domain-Name : service : serviceType : version où Domain-Name est un nom de domaine qui est enregistré auprès du fournisseur.

</dd> <dt>

<span id="upnp.s_5_gly"></span><span id="UPNP.S_5_GLY"></span>**variable d’État**
</dt> <dd>

Une variable d’État est un élément de données qui décrit une partie de l’état d’un service.

</dd> </dl>

 

 




