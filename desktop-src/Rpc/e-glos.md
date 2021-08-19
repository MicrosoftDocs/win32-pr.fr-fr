---
title: E (RPC)
description: Mots commençant par E dans le glossaire de l’appel de procédure distante (RPC).
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 76e35c3c-91dd-42e3-9699-6767e37b2699
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df69c06e72a84207cffd7c708cea3673a3cb33e2d6eea477024a7c66963b3878
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930515"
---
# <a name="e-rpc"></a>E (RPC)

[A](a-glos.md) [B](b-glos.md) [C](c-glos.md) [D](d-glos.md) e [F](f-glos.md) G H [I](i-glos.md) J K [L](l-glos.md) [M](m-glos.md) [N](n-glos.md) [O](o-glos.md) [P](p-glos.md) [Q](q.md) [R](r-glos.md) [S](s-glos.md) [T](t-glos.md) [U](u-glos.md) [V](v-glos.md) [W](w-glos.md) X Y Z

<dl> <dt>

<span id="_rpc_embedded_pointer_glos"></span><span id="_RPC_EMBEDDED_POINTER_GLOS"></span>**pointeur incorporé**
</dt> <dd>

Pointeur incorporé dans un paramètre qui est une structure de données telle qu’un tableau, une structure ou une Union. Voir aussi [*pointeur de niveau supérieur*](t-glos.md).

</dd> <dt>

<span id="_rpc_encoding_services_glos"></span><span id="_RPC_ENCODING_SERVICES_GLOS"></span>**services d’encodage**
</dt> <dd>

Routines de stub générées par MIDL qui assurent la prise en charge de l’encodage et du décodage des données (également appelées *récupération* ou *sérialisation*). Permet aux programmeurs de contrôler les mémoires tampons contenant des données à marshaler et à démarshaler. Voir aussi [*sérialisation de type*](t-glos.md), [*sérialisation de procédure*](p-glos.md).

</dd> <dt>

<span id="_rpc_endpoint_glos"></span><span id="_RPC_ENDPOINT_GLOS"></span>**poste**
</dt> <dd>

Adresse spécifique au réseau d’un processus serveur pour les appels de procédure distante. Le nom réel du point de terminaison dépend de la séquence de protocole utilisée. Voir aussi [*point de terminaison dynamique*](d-glos.md) et [*point de terminaison connu*](w-glos.md).

</dd> <dt>

<span id="_rpc_endpoint_mapper_glos"></span><span id="_RPC_ENDPOINT_MAPPER_GLOS"></span>**mappeur de point de terminaison**
</dt> <dd>

Partie du sous-système RPC (RPCSS) qui permet à la bibliothèque Runtime d’assigner et de résoudre dynamiquement des points de terminaison. Voir aussi [point de terminaison](/windows).

</dd> <dt>

<span id="_rpc_encapsulated_union_glos"></span><span id="_RPC_ENCAPSULATED_UNION_GLOS"></span>**Union encapsulée**
</dt> <dd>

Construction MIDL qui permet de passer des unions dans le cadre d’un appel de procédure distante en incorporant l’Union dans une structure dans laquelle le discriminante est le premier champ de la structure, et l’Union est le deuxième champ (et final) de la structure. Le **commutateur** de mot clé [*IDL*](i-glos.md) spécifie qu’une Union est encapsulée. Voir aussi [*Union unencapsulée*](n-glos.md).

</dd> <dt>

<span id="_rpc_epv_glos"></span><span id="_RPC_EPV_GLOS"></span>**vecteur de point d’entrée (EPV)**
</dt> <dd>

Tableau de pointeurs vers des fonctions qui implémentent les opérations spécifiées dans l’interface. Chaque élément du tableau correspond à une fonction définie dans le fichier IDL. Les vecteurs de point d’entrée permettent aux applications distribuées de prendre en charge plusieurs implémentations des fonctions définies dans le fichier IDL.

</dd> </dl>

 

 
