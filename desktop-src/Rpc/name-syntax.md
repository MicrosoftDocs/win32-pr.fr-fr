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
# <a name="name-syntax"></a><span data-ttu-id="2379e-103">Syntaxe de nom</span><span class="sxs-lookup"><span data-stu-id="2379e-103">Name Syntax</span></span>

<span data-ttu-id="2379e-104">Microsoft RPC accepte les noms conformes à la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="2379e-104">Microsoft RPC accepts names that conform to the following syntax:</span></span>

``` syntax
/.:/name[/name...]/.../domainname/name[/name...]
```

## <a name="parameters"></a><span data-ttu-id="2379e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2379e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2379e-106"><span id="name"></span><span id="NAME"></span>nomme</span><span class="sxs-lookup"><span data-stu-id="2379e-106"><span id="name"></span><span id="NAME"></span>name</span></span>
</dt> <dd>

<span data-ttu-id="2379e-107">Spécifie un identificateur qui peut contenir n’importe quel caractère à l’exception du caractère de barre oblique (/) de délimitation.</span><span class="sxs-lookup"><span data-stu-id="2379e-107">Specifies an identifier that can contain any character except the delimiting slash (/) character.</span></span>

</dd> <dt>

<span data-ttu-id="2379e-108"><span id="domainname"></span><span id="DOMAINNAME"></span>NomDomaine</span><span class="sxs-lookup"><span data-stu-id="2379e-108"><span id="domainname"></span><span id="DOMAINNAME"></span>domainname</span></span>
</dt> <dd>

<span data-ttu-id="2379e-109">Spécifie le nom du domaine.</span><span class="sxs-lookup"><span data-stu-id="2379e-109">Specifies the name of the domain.</span></span>

</dd> </dl>

<span data-ttu-id="2379e-110">Paramètre qui sélectionne le type de syntaxe de nom et la chaîne qui spécifie que le nom est fourni à la plupart des fonctions RPC NSI (Name Service Interface).</span><span class="sxs-lookup"><span data-stu-id="2379e-110">A parameter that selects the name-syntax type and the string that specifies the name are supplied to many of the name service interface (NSI) RPC functions.</span></span>

<span data-ttu-id="2379e-111">Un seul type de syntaxe de nom est pris en charge par Microsoft RPC, comme spécifié par l’ETCD de syntaxe RPC C de la constante RPC \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2379e-111">Only one name-syntax type is supported by Microsoft RPC, as specified by the constant RPC\_C\_NS\_SYNTAX\_DCE.</span></span> <span data-ttu-id="2379e-112">Cette constante est définie dans le fichier d’en-tête RPCNSI. H.</span><span class="sxs-lookup"><span data-stu-id="2379e-112">This constant is defined in the header file RPCNSI.H.</span></span>

<span data-ttu-id="2379e-113">La syntaxe de nom spécifiée par \_ le \_ DCE de la syntaxe RPC C NS \_ \_ est une extension de la syntaxe du nom de l’service D’ANNUAIRE de cellules/service D’ANNUAIRES de cellules de l' \_ ETCD OSF (CDS).</span><span class="sxs-lookup"><span data-stu-id="2379e-113">The name syntax specified by RPC\_C\_NS\_SYNTAX\_DCE is an extension of the OSF\_DCE Cell Directory Service (CDS) name syntax.</span></span> <span data-ttu-id="2379e-114">La possibilité de spécifier un nom de domaine représente une extension de cette syntaxe.</span><span class="sxs-lookup"><span data-stu-id="2379e-114">The ability to specify a domain name represents an extension to that syntax.</span></span> <span data-ttu-id="2379e-115">Il n’existe aucune limite absolue quant au nombre de noms qui peuvent être séparés par des barres obliques, à condition que la chaîne globale soit inférieure à 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="2379e-115">There is no absolute limit on the number of names that can be separated by slash characters as long as the overall string is less than 256 characters.</span></span>

<span data-ttu-id="2379e-116">Les barres obliques vous permettent de spécifier une structure logique pour le nom, mais elles ne correspondent pas à une structure logique dans les objets eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="2379e-116">The slashes allow you to specify a logical structure to the name, but they do not correspond to a logical structure in the objects themselves.</span></span>

 

 




