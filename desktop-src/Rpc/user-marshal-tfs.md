---
title: Marshal d’utilisateur
description: Utilisateur-Marshal dans l’appel de procédure distante (RPC).
ms.assetid: 5119e959-d8b8-4fca-8910-568bb9063a9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c901fd8c75137b4657322a89692ff8a3afb5408
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840025"
---
# <a name="user-marshal"></a><span data-ttu-id="cd45d-103">Marshal d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="cd45d-103">User-marshal</span></span>

<span data-ttu-id="cd45d-104">Le Marshal utilisateur a une chaîne de format similaire à la transmission \_ en tant que :</span><span class="sxs-lookup"><span data-stu-id="cd45d-104">User marshal has a format string that is similar to transmit\_as:</span></span>

``` syntax
FC_USER_MARSHAL
flags<1>
quadruple_index<2>
user_type_memory_size<2>
transmitted_type_buffer size<2>
offset_to_the_transmitted_type<2>
```

<span data-ttu-id="cd45d-105">Les indicateurs<1> octet se composent du Quartet indicateur supérieur et du Quartet alignement inférieur.</span><span class="sxs-lookup"><span data-stu-id="cd45d-105">The flags<1> byte consists of the upper flag nibble and the lower alignment nibble.</span></span>

<span data-ttu-id="cd45d-106">Les 2 bits supérieurs du Quartet d’indicateur sont utilisés pour décrire si le type de câble est défini comme pointeur unique, pointeur de référence ou sans pointeur (il ne peut pas être un PTR).</span><span class="sxs-lookup"><span data-stu-id="cd45d-106">The upper 2 bits of the flag nibble are used to describe whether the wire type is defined as a unique pointer, reference pointer or no pointer (it cannot be a ptr).</span></span> <span data-ttu-id="cd45d-107">Les manifestes suivants ont été définis pour définir/obtenir les indicateurs :</span><span class="sxs-lookup"><span data-stu-id="cd45d-107">The following manifests have been defined to set/get the flags:</span></span>

``` syntax
#define USER_MARSHAL_UNIQUE         0x80
#define USER_MARSHAL_REF            0x40
#define USER_MARSHAL_POINTER        0xc0  /* unique or ref */
#define USER_MARSHAL_IID            0x20  /* JIT compiler only */
```

<span data-ttu-id="cd45d-108">Le grignot d’alignement du mot d’indicateur conserve l’alignement filaire du type transmis.</span><span class="sxs-lookup"><span data-stu-id="cd45d-108">The alignment nibble of the flag word keeps the wire alignment of the transmitted type.</span></span>

<span data-ttu-id="cd45d-109">L’index quadruple \_<2> est un index de la routine de rappel quadruple des fonctions de Marshal utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cd45d-109">The quadruple\_index<2> is an index of the callback routine quadruple of the user marshal functions.</span></span> <span data-ttu-id="cd45d-110">Les positions de routine sont les suivantes : dimensionnement, marshaling, démarshaling et routine de libération.</span><span class="sxs-lookup"><span data-stu-id="cd45d-110">The routine positions are as follow: sizing, marshaling, unmarshaling, and freeing routine.</span></span>

<span data-ttu-id="cd45d-111">La \_ \_ taille de la mémoire de type utilisateur \_<2> fournit une taille pour le type spécifique de l’utilisateur, y compris les types inconnus.</span><span class="sxs-lookup"><span data-stu-id="cd45d-111">The user\_type\_memory\_size<2> provides a size for the user specific type, including unknown types.</span></span>

<span data-ttu-id="cd45d-112">La taille de la \_ mémoire tampon de type transmis \_ \_<2> est soit zéro lorsque la taille est variable, soit la taille fixe réelle.</span><span class="sxs-lookup"><span data-stu-id="cd45d-112">The transmitted\_type\_buffer\_size<2> is either zero when the size is varying, or the actual fixed size.</span></span> <span data-ttu-id="cd45d-113">Il s’agit d’une optimisation qui permet à MIDL d’ignorer les rappels lors du dimensionnement de la mémoire tampon, ainsi que lors de la libération de.</span><span class="sxs-lookup"><span data-stu-id="cd45d-113">This is an optimization that enables MIDL to skip callbacks when sizing the buffer, and also when freeing.</span></span>

## <a name="range"></a><span data-ttu-id="cd45d-114">Plage</span><span class="sxs-lookup"><span data-stu-id="cd45d-114">Range</span></span>

<span data-ttu-id="cd45d-115">La \[ \] vérification de plage fournit des moyens supplémentaires pour la validation d’argument au niveau de la couche NDR.</span><span class="sxs-lookup"><span data-stu-id="cd45d-115">The \[range\] checking provides additional means for argument validation at the NDR layer.</span></span> <span data-ttu-id="cd45d-116">Le \[ \] descripteur de plage a le format suivant :</span><span class="sxs-lookup"><span data-stu-id="cd45d-116">The \[range\] descriptor has the following format:</span></span>

``` syntax
FC_RANGE,   flags_type <1>
low value<4>
high value<4>
```

<span data-ttu-id="cd45d-117">Les indicateurs prennent le Quartet supérieur et le type le Quartet inférieur du deuxième octet.</span><span class="sxs-lookup"><span data-stu-id="cd45d-117">The flags take the upper nibble and the type the lower nibble of the second byte.</span></span> <span data-ttu-id="cd45d-118">Les valeurs basse et haute dépendent du type de la variable à vérifier.</span><span class="sxs-lookup"><span data-stu-id="cd45d-118">The low and high values depend on the type of the variable to be checked.</span></span>

<span data-ttu-id="cd45d-119">Les indicateurs sont conçus comme un véhicule d’expansion ; le compilateur a défini le Quartet sur zéro.</span><span class="sxs-lookup"><span data-stu-id="cd45d-119">The flags are meant as an expansion vehicle; the compiler has been setting the nibble to zero.</span></span>

 

 




