---
title: Génération d’UUID d’interface
description: Génération d’identificateurs uniques universels (UUID) d’interface et utilisation de uuidgen.
ms.assetid: a973b7f9-71c5-46a0-aa0c-51f150560dbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68c5f727ed3e37139d4da50f84c3929bff333156
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673002"
---
# <a name="generating-interface-uuids"></a><span data-ttu-id="12e57-103">Génération d’UUID d’interface</span><span class="sxs-lookup"><span data-stu-id="12e57-103">Generating Interface UUIDs</span></span>

<span data-ttu-id="12e57-104">Cette section fournit des informations sur les identificateurs uniques universels (UUID) et l’utilitaire uuidgen dans les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="12e57-104">This section presents information on Universal Unique Identifiers (UUIDs) and the Uuidgen utility in the following topics:</span></span>

-   [<span data-ttu-id="12e57-105">Qu’est-ce qu’un UUID ?</span><span class="sxs-lookup"><span data-stu-id="12e57-105">What is a UUID?</span></span>](#what-is-a-uuid)
-   [<span data-ttu-id="12e57-106">Utilisation de uuidgen</span><span class="sxs-lookup"><span data-stu-id="12e57-106">Using Uuidgen</span></span>](#using-uuidgen)

## <a name="what-is-a-uuid"></a><span data-ttu-id="12e57-107">Qu’est-ce qu’un UUID ?</span><span class="sxs-lookup"><span data-stu-id="12e57-107">What is a UUID?</span></span>

<span data-ttu-id="12e57-108">Toutes les interfaces doivent être identifiées de manière unique sur un réseau afin que les clients puissent les trouver.</span><span class="sxs-lookup"><span data-stu-id="12e57-108">All interfaces must be uniquely identified on a network so that clients can find them.</span></span> <span data-ttu-id="12e57-109">Sur les réseaux de petite taille, le nom de l’interface seul peut suffire pour l’identifier.</span><span class="sxs-lookup"><span data-stu-id="12e57-109">On small networks, the interface's name alone may be sufficient to identify it.</span></span> <span data-ttu-id="12e57-110">Toutefois, cela n’est généralement pas possible sur les réseaux de grande taille.</span><span class="sxs-lookup"><span data-stu-id="12e57-110">However, that is usually not feasible on large networks.</span></span> <span data-ttu-id="12e57-111">Par conséquent, les développeurs attribuent généralement un identificateur unique universel (UUID, interchangeable avec le terme GUID ou un identificateur global unique) à chaque interface.</span><span class="sxs-lookup"><span data-stu-id="12e57-111">Therefore, developers typically assign a Universal Unique Identifier (UUID, interchangeable with the term GUID, or Globally Unique Identifier) to each interface.</span></span> <span data-ttu-id="12e57-112">Un UUID est une chaîne qui contient un jeu de chiffres hexadécimaux.</span><span class="sxs-lookup"><span data-stu-id="12e57-112">A UUID is a string that contains a set of hexadecimal digits.</span></span> <span data-ttu-id="12e57-113">Chaque interface possède un UUID différent.</span><span class="sxs-lookup"><span data-stu-id="12e57-113">Each interface has a different UUID.</span></span> <span data-ttu-id="12e57-114">Pour plus d’informations, consultez [UUID de chaîne](string-uuid.md).</span><span class="sxs-lookup"><span data-stu-id="12e57-114">For details, see [String UUID](string-uuid.md).</span></span>

<span data-ttu-id="12e57-115">La représentation textuelle d’un UUID est une chaîne composée de 8 chiffres hexadécimaux suivis d’un trait d’Union, suivi de trois groupes séparés par des tirets de 4 chiffres hexadécimaux, suivis d’un trait d’Union, suivi de 12 chiffres hexadécimaux.</span><span class="sxs-lookup"><span data-stu-id="12e57-115">The textual representation of a UUID is a string consisting of 8 hexadecimal digits followed by a hyphen, followed by three hyphen-separated groups of 4 hexadecimal digits, followed by a hyphen, followed by 12 hexadecimal digits.</span></span> <span data-ttu-id="12e57-116">L’exemple suivant est une chaîne UUID valide :</span><span class="sxs-lookup"><span data-stu-id="12e57-116">The following example is a valid UUID string:</span></span>

<span data-ttu-id="12e57-117">ba209999-0c6c-11d2-97cf-00c04f8eea45</span><span class="sxs-lookup"><span data-stu-id="12e57-117">ba209999-0c6c-11d2-97cf-00c04f8eea45</span></span>

<span data-ttu-id="12e57-118">Les UUID vides sont appelés UUID nuls et non **null** .</span><span class="sxs-lookup"><span data-stu-id="12e57-118">Empty UUIDs are referred to as nil UUIDs rather than **NULL** UUIDs.</span></span> <span data-ttu-id="12e57-119">Le terme « Nil » indique tout ce qui est zéro, vide, vide ou non initialisé.</span><span class="sxs-lookup"><span data-stu-id="12e57-119">The term nil indicates anything that is zero, blank, empty, or uninitialized.</span></span> <span data-ttu-id="12e57-120">Une chaîne vide, un enregistrement de base de données vide ou un UUID non initialisé sont des exemples de valeurs Nil.</span><span class="sxs-lookup"><span data-stu-id="12e57-120">An empty string, an empty database record, or an uninitialized UUID are all examples of nil values.</span></span>

> [!Note]  
> <span data-ttu-id="12e57-121">La valeur **null** correspond à la valeur zéro spécifique.</span><span class="sxs-lookup"><span data-stu-id="12e57-121">The value **NULL** is the specific value zero.</span></span> <span data-ttu-id="12e57-122">Il est souvent utilisé dans la programmation C et C++ conjointement avec les pointeurs.</span><span class="sxs-lookup"><span data-stu-id="12e57-122">It is often used in C and C++ programming in conjunction with pointers.</span></span> <span data-ttu-id="12e57-123">Nil est un terme plus général que **null**.</span><span class="sxs-lookup"><span data-stu-id="12e57-123">Nil is a more general term than **NULL**.</span></span> <span data-ttu-id="12e57-124">Les UUID non initialisés de l’interface d’objet doivent toujours être appelés UUID NULL plutôt que des UUID **null** .</span><span class="sxs-lookup"><span data-stu-id="12e57-124">Uninitialized object interface UUIDs should always be referred to as nil UUIDs rather than **NULL** UUIDs.</span></span>

 

## <a name="using-uuidgen"></a><span data-ttu-id="12e57-125">Utilisation de uuidgen</span><span class="sxs-lookup"><span data-stu-id="12e57-125">Using Uuidgen</span></span>

<span data-ttu-id="12e57-126">Microsoft fournit un programme utilitaire appelé uuidgen pour générer vos UUID.</span><span class="sxs-lookup"><span data-stu-id="12e57-126">Microsoft provides a utility program called Uuidgen to generate your UUIDs.</span></span> <span data-ttu-id="12e57-127">L’utilitaire uuidgen génère l’UUID au format de fichier IDL ou au format de langage C.</span><span class="sxs-lookup"><span data-stu-id="12e57-127">The Uuidgen utility generates the UUID in IDL file format or C-language format.</span></span>

<span data-ttu-id="12e57-128">Quand vous exécutez l’utilitaire uuidgen à partir de la ligne de commande, vous pouvez utiliser les commutateurs de commande suivants.</span><span class="sxs-lookup"><span data-stu-id="12e57-128">When you run the Uuidgen utility from the command line, you can use the following command switches.</span></span>



| <span data-ttu-id="12e57-129">Commutateur uuidgen</span><span class="sxs-lookup"><span data-stu-id="12e57-129">Uuidgen switch</span></span>           | <span data-ttu-id="12e57-130">Description</span><span class="sxs-lookup"><span data-stu-id="12e57-130">Description</span></span>                                                                |
|--------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="12e57-131">**/I**</span><span class="sxs-lookup"><span data-stu-id="12e57-131">**/I**</span></span>                   | <span data-ttu-id="12e57-132">Génère l’UUID dans un modèle d’interface IDL.</span><span class="sxs-lookup"><span data-stu-id="12e57-132">Outputs UUID to an IDL interface template.</span></span>                                 |
| <span data-ttu-id="12e57-133">**commutateur**</span><span class="sxs-lookup"><span data-stu-id="12e57-133">**/s**</span></span>                   | <span data-ttu-id="12e57-134">Génère l’UUID en tant que structure C initialisée.</span><span class="sxs-lookup"><span data-stu-id="12e57-134">Outputs UUID as an initialized C structure.</span></span>                                |
| <span data-ttu-id="12e57-135">**/o** < *nom du fichier*></span><span class="sxs-lookup"><span data-stu-id="12e57-135">**/o**<*filename*></span></span> | <span data-ttu-id="12e57-136">Redirige la sortie vers un fichier ; spécifié immédiatement après le commutateur **/o** .</span><span class="sxs-lookup"><span data-stu-id="12e57-136">Redirects output to a file; specified immediately after the **/o** switch.</span></span> |
| <span data-ttu-id="12e57-137">**/n** < *nombre*></span><span class="sxs-lookup"><span data-stu-id="12e57-137">**/n**<*number*></span></span>   | <span data-ttu-id="12e57-138">Spécifie le nombre d’UUID à générer.</span><span class="sxs-lookup"><span data-stu-id="12e57-138">Specifies the number of UUIDs to generate.</span></span>                                 |
| <span data-ttu-id="12e57-139">**/v**</span><span class="sxs-lookup"><span data-stu-id="12e57-139">**/v**</span></span>                   | <span data-ttu-id="12e57-140">Affiche des informations de version sur uuidgen.</span><span class="sxs-lookup"><span data-stu-id="12e57-140">Displays version information about Uuidgen.</span></span>                                |
| <span data-ttu-id="12e57-141">**/h** ou **?**</span><span class="sxs-lookup"><span data-stu-id="12e57-141">**/h** or **?**</span></span>          | <span data-ttu-id="12e57-142">Affiche le résumé des options de commande.</span><span class="sxs-lookup"><span data-stu-id="12e57-142">Displays command-option summary.</span></span>                                           |



 

<span data-ttu-id="12e57-143">En général, vous allez utiliser l’utilitaire uuidgen comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="12e57-143">Typically, you will use the Uuidgen utility as shown in the following example.</span></span>

<span data-ttu-id="12e57-144">**uuidgen-i-oMyApp. idl**</span><span class="sxs-lookup"><span data-stu-id="12e57-144">**uuidgen -i -oMyApp.idl**</span></span>

<span data-ttu-id="12e57-145">Cette commande génère un UUID et le stocke dans un fichier MIDL que vous pouvez utiliser comme modèle.</span><span class="sxs-lookup"><span data-stu-id="12e57-145">This command generates a UUID and stores it in a MIDL file that you can use as a template.</span></span> <span data-ttu-id="12e57-146">Lorsque la commande précédente est exécutée, le contenu de MyApp. idl est semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="12e57-146">When the preceding command is executed, the contents of MyApp.idl are similar to the following:</span></span>

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface INTERFACENAME
{

}
```

<span data-ttu-id="12e57-147">L’étape suivante consiste à remplacer le nom de l’espace réservé, NOMINTERFACE, par le nom réel de votre interface.</span><span class="sxs-lookup"><span data-stu-id="12e57-147">The next step would be to replace the placeholder name, INTERFACENAME, with the actual name of your interface.</span></span>

 

 




