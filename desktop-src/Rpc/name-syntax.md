---
title: Syntaxe de nom
description: La syntaxe de l’appel de procédure distante (RPC) et du nom.
ms.assetid: eb370106-bd88-4c21-b287-7b2b174185d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d024130a5b8a873c6bfbb2194542344953625d5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940147"
---
# <a name="name-syntax"></a>Syntaxe de nom

Microsoft RPC accepte les noms conformes à la syntaxe suivante :

``` syntax
/.:/name[/name...]/.../domainname/name[/name...]
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="name"></span><span id="NAME"></span>nomme
</dt> <dd>

Spécifie un identificateur qui peut contenir n’importe quel caractère à l’exception du caractère de barre oblique (/) de délimitation.

</dd> <dt>

<span id="domainname"></span><span id="DOMAINNAME"></span>NomDomaine
</dt> <dd>

Spécifie le nom du domaine.

</dd> </dl>

Paramètre qui sélectionne le type de syntaxe de nom et la chaîne qui spécifie que le nom est fourni à la plupart des fonctions RPC NSI (Name Service Interface).

Un seul type de syntaxe de nom est pris en charge par Microsoft RPC, comme spécifié par l’ETCD de syntaxe RPC C de la constante RPC \_ \_ \_ \_ . Cette constante est définie dans le fichier d’en-tête RPCNSI. H.

La syntaxe de nom spécifiée par \_ le \_ DCE de la syntaxe RPC C NS \_ \_ est une extension de la syntaxe du nom de l’service D’ANNUAIRE de cellules/service D’ANNUAIRES de cellules de l' \_ ETCD OSF (CDS). La possibilité de spécifier un nom de domaine représente une extension de cette syntaxe. Il n’existe aucune limite absolue quant au nombre de noms qui peuvent être séparés par des barres obliques, à condition que la chaîne globale soit inférieure à 256 caractères.

Les barres obliques vous permettent de spécifier une structure logique pour le nom, mais elles ne correspondent pas à une structure logique dans les objets eux-mêmes.

 

 




