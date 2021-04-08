---
description: 'Les modèles définissent la façon dont le flux de données est interprété : les données sont modulées par la définition du modèle. Cette section décrit les aspects suivants d’un modèle et fournit un exemple de modèle.'
ms.assetid: f84978a8-8315-4626-be68-f00f3a72e5ac
title: Modèles (format de fichier X, encodage de texte)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fccec46e72a73bb5ed4434fd252595e1b072ad4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745389"
---
# <a name="templates-x-file-format-text-encoding"></a><span data-ttu-id="4c401-104">Modèles (format de fichier X, encodage de texte)</span><span class="sxs-lookup"><span data-stu-id="4c401-104">Templates (X file format, text encoding)</span></span>

<span data-ttu-id="4c401-105">Les modèles définissent la façon dont le flux de données est interprété : les données sont modulées par la définition du modèle.</span><span class="sxs-lookup"><span data-stu-id="4c401-105">Templates define how the data stream is interpreted - the data is modulated by the template definition.</span></span> <span data-ttu-id="4c401-106">Cette section décrit les aspects suivants d’un modèle et fournit un exemple de modèle.</span><span class="sxs-lookup"><span data-stu-id="4c401-106">This section discusses the following aspects of a template and provides an example template.</span></span>

<span data-ttu-id="4c401-107">Il existe un modèle spécial : le modèle d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="4c401-107">There is one special template - the header template.</span></span> <span data-ttu-id="4c401-108">Il est recommandé que chaque application définisse un modèle d’en-tête et l’utilise pour définir des informations spécifiques à l’application, telles que des informations de version.</span><span class="sxs-lookup"><span data-stu-id="4c401-108">It is recommended that each application define a header template and use it to define application-specific information, such as version information.</span></span> <span data-ttu-id="4c401-109">S’il est présent, cet en-tête est lu par l’API de format de fichier. x.</span><span class="sxs-lookup"><span data-stu-id="4c401-109">If present, this header is read by the .x file format API.</span></span> <span data-ttu-id="4c401-110">Si un membre indicateurs est disponible, il est utilisé pour déterminer comment les données suivantes sont interprétées.</span><span class="sxs-lookup"><span data-stu-id="4c401-110">If a flags member is available, it is used to determine how the following data is interpreted.</span></span> <span data-ttu-id="4c401-111">Le membre Flags, s’il est défini, doit être une valeur DWORD.</span><span class="sxs-lookup"><span data-stu-id="4c401-111">The flags member, if defined, should be a DWORD.</span></span> <span data-ttu-id="4c401-112">Un bit est actuellement défini-bit 0.</span><span class="sxs-lookup"><span data-stu-id="4c401-112">One bit is currently defined - bit 0.</span></span> <span data-ttu-id="4c401-113">Si ce bit est clair, les données suivantes dans le fichier sont binaires.</span><span class="sxs-lookup"><span data-stu-id="4c401-113">If this bit is clear, the following data in the file is binary.</span></span> <span data-ttu-id="4c401-114">Si cette valeur est définie, les données suivantes sont du texte.</span><span class="sxs-lookup"><span data-stu-id="4c401-114">If set, the following data is text.</span></span> <span data-ttu-id="4c401-115">Vous pouvez utiliser plusieurs objets de données d’en-tête pour basculer entre le binaire et le texte dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="4c401-115">You can use multiple header data objects to switch between binary and text within the file.</span></span>

## <a name="template-form-name-and-uuid"></a><span data-ttu-id="4c401-116">Formulaire, nom et UUID du modèle</span><span class="sxs-lookup"><span data-stu-id="4c401-116">Template Form, Name, and UUID</span></span>

<span data-ttu-id="4c401-117">Un modèle se présente sous la forme suivante.</span><span class="sxs-lookup"><span data-stu-id="4c401-117">A template has the following form.</span></span>


```
template <template-name> {
<UUID>
    <member 1>;
...
    <member n>;
[restrictions]
}
```



<span data-ttu-id="4c401-118">Le nom du modèle est un nom alphanumérique qui peut inclure le trait de soulignement ( \_ ).</span><span class="sxs-lookup"><span data-stu-id="4c401-118">The template name is an alphanumeric name that can include the underscore character (\_).</span></span> <span data-ttu-id="4c401-119">Il ne doit pas commencer par un chiffre.</span><span class="sxs-lookup"><span data-stu-id="4c401-119">It must not begin with a digit.</span></span> <span data-ttu-id="4c401-120">L’UUID est un identificateur unique universel mis en forme dans l’environnement de calcul distribué (Open Software Foundation) standard et placé entre crochets (< >).</span><span class="sxs-lookup"><span data-stu-id="4c401-120">The UUID is a universally unique identifier formatted to the Open Software Foundation's Distributed Computing Environment standard and enclosed by angle brackets (< >).</span></span> <span data-ttu-id="4c401-121">Par exemple : <> 3D82AB43-62DA-11cf-AB39-0020AF71E433.</span><span class="sxs-lookup"><span data-stu-id="4c401-121">For example: <3D82AB43-62DA-11cf-AB39-0020AF71E433>.</span></span>

## <a name="template-members"></a><span data-ttu-id="4c401-122">Membres du modèle</span><span class="sxs-lookup"><span data-stu-id="4c401-122">Template Members</span></span>

<span data-ttu-id="4c401-123">Les membres de modèles se composent d’un type de données nommé suivi d’un nom facultatif ou d’un tableau d’un type de données nommé.</span><span class="sxs-lookup"><span data-stu-id="4c401-123">Template members consist of a named data type followed by an optional name or an array of a named data type.</span></span> <span data-ttu-id="4c401-124">Les types de données primitifs valides sont définis dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4c401-124">Valid primitive data types are defined in the following table.</span></span>



| <span data-ttu-id="4c401-125">Type</span><span class="sxs-lookup"><span data-stu-id="4c401-125">Type</span></span>    | <span data-ttu-id="4c401-126">Taille</span><span class="sxs-lookup"><span data-stu-id="4c401-126">Size</span></span>                               |
|---------|------------------------------------|
| <span data-ttu-id="4c401-127">WORD</span><span class="sxs-lookup"><span data-stu-id="4c401-127">WORD</span></span>    | <span data-ttu-id="4c401-128">16 bits</span><span class="sxs-lookup"><span data-stu-id="4c401-128">16 bits</span></span>                            |
| <span data-ttu-id="4c401-129">DWORD</span><span class="sxs-lookup"><span data-stu-id="4c401-129">DWORD</span></span>   | <span data-ttu-id="4c401-130">32 bits</span><span class="sxs-lookup"><span data-stu-id="4c401-130">32 bits</span></span>                            |
| <span data-ttu-id="4c401-131">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4c401-131">FLOAT</span></span>   | <span data-ttu-id="4c401-132">FLOTTE IEEE</span><span class="sxs-lookup"><span data-stu-id="4c401-132">IEEE float</span></span>                         |
| <span data-ttu-id="4c401-133">DOUBLE</span><span class="sxs-lookup"><span data-stu-id="4c401-133">DOUBLE</span></span>  | <span data-ttu-id="4c401-134">64 bits</span><span class="sxs-lookup"><span data-stu-id="4c401-134">64 bits</span></span>                            |
| <span data-ttu-id="4c401-135">CHAR</span><span class="sxs-lookup"><span data-stu-id="4c401-135">CHAR</span></span>    | <span data-ttu-id="4c401-136">8 bits</span><span class="sxs-lookup"><span data-stu-id="4c401-136">8 bits</span></span>                             |
| <span data-ttu-id="4c401-137">UCHAR</span><span class="sxs-lookup"><span data-stu-id="4c401-137">UCHAR</span></span>   | <span data-ttu-id="4c401-138">8 bits</span><span class="sxs-lookup"><span data-stu-id="4c401-138">8 bits</span></span>                             |
| <span data-ttu-id="4c401-139">BYTE</span><span class="sxs-lookup"><span data-stu-id="4c401-139">BYTE</span></span>    | <span data-ttu-id="4c401-140">8 bits</span><span class="sxs-lookup"><span data-stu-id="4c401-140">8 bits</span></span>                             |
| <span data-ttu-id="4c401-141">STRING</span><span class="sxs-lookup"><span data-stu-id="4c401-141">STRING</span></span>  | <span data-ttu-id="4c401-142">Chaîne terminée par NULL</span><span class="sxs-lookup"><span data-stu-id="4c401-142">NULL terminated string</span></span>             |
| <span data-ttu-id="4c401-143">CSTRING</span><span class="sxs-lookup"><span data-stu-id="4c401-143">CSTRING</span></span> | <span data-ttu-id="4c401-144">Chaîne C mise en forme (non prise en charge)</span><span class="sxs-lookup"><span data-stu-id="4c401-144">Formatted C string (not supported)</span></span> |
| <span data-ttu-id="4c401-145">UNICODE</span><span class="sxs-lookup"><span data-stu-id="4c401-145">UNICODE</span></span> | <span data-ttu-id="4c401-146">Chaîne Unicode (non prise en charge)</span><span class="sxs-lookup"><span data-stu-id="4c401-146">Unicode string (not supported)</span></span>     |



 

<span data-ttu-id="4c401-147">Les types de données supplémentaires définis par les modèles rencontrés précédemment dans le flux de données peuvent également être référencés dans une définition de modèle.</span><span class="sxs-lookup"><span data-stu-id="4c401-147">Additional data types defined by templates encountered earlier in the data stream can also be referenced within a template definition.</span></span> <span data-ttu-id="4c401-148">Aucune référence anticipée n’est autorisée.</span><span class="sxs-lookup"><span data-stu-id="4c401-148">No forward references are allowed.</span></span>

<span data-ttu-id="4c401-149">Tous les types de données valides peuvent être exprimés sous la forme d’un tableau dans la définition du modèle.</span><span class="sxs-lookup"><span data-stu-id="4c401-149">Any valid data type can be expressed as an array in the template definition.</span></span> <span data-ttu-id="4c401-150">La syntaxe de base est illustrée dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="4c401-150">The basic syntax is shown in the following example.</span></span>


```
array <data-type> <name>[<dimension-size>];
```



<span data-ttu-id="4c401-151"><dimension-size> peut être un entier ou une référence nommée à un autre membre de modèle dont la valeur est ensuite substituée.</span><span class="sxs-lookup"><span data-stu-id="4c401-151"><dimension-size> can either be an integer or a named reference to another template member whose value is then substituted.</span></span> <span data-ttu-id="4c401-152">Les tableaux peuvent être multidimensionnels, où n est déterminé par le nombre de crochets appariés à la fin de l’instruction, comme dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="4c401-152">Arrays can be n-dimensional, where n is determined by the number of paired square brackets trailing the statement, as in the following example.</span></span>


```
array DWORD FixedHerd[24];
array DWORD Herd[nCows];
array FLOAT Matrix4x4[4][4];
```



## <a name="template-restrictions"></a><span data-ttu-id="4c401-153">Restrictions de modèle</span><span class="sxs-lookup"><span data-stu-id="4c401-153">Template Restrictions</span></span>

<span data-ttu-id="4c401-154">Les modèles peuvent être ouverts, fermés ou restreints.</span><span class="sxs-lookup"><span data-stu-id="4c401-154">Templates can be open, closed, or restricted.</span></span> <span data-ttu-id="4c401-155">Ces restrictions déterminent les types de données qui peuvent apparaître dans la hiérarchie immédiate d’un objet de données défini par le modèle.</span><span class="sxs-lookup"><span data-stu-id="4c401-155">These restrictions determine which data types can appear in the immediate hierarchy of a data object defined by the template.</span></span> <span data-ttu-id="4c401-156">Un modèle ouvert n’a aucune restriction, un modèle fermé rejette tous les types de données et un modèle restreint autorise une liste nommée de types de données.</span><span class="sxs-lookup"><span data-stu-id="4c401-156">An open template has no restrictions, a closed template rejects all data types, and a restricted template allows a named list of data types.</span></span>

<span data-ttu-id="4c401-157">La syntaxe permettant d’indiquer qu’un modèle est ouvert est de trois points délimités par des crochets.</span><span class="sxs-lookup"><span data-stu-id="4c401-157">The syntax for indicating an open template is three periods enclosed by square brackets.</span></span>


```
[ ... ]
```



<span data-ttu-id="4c401-158">Une liste séparée par des virgules de types de données nommés suivi éventuellement de leurs UUID délimités par des crochets indique un modèle restreint.</span><span class="sxs-lookup"><span data-stu-id="4c401-158">A comma-separated list of named data types followed optionally by their UUIDs enclosed by square brackets indicates a restricted template.</span></span>


```
[ { data-type [ UUID ] , } ... ]
```



<span data-ttu-id="4c401-159">L’absence de l’un des éléments ci-dessus indique un modèle fermé.</span><span class="sxs-lookup"><span data-stu-id="4c401-159">The absence of either of the above indicates a closed template.</span></span>

## <a name="template-example"></a><span data-ttu-id="4c401-160">Exemple de modèle</span><span class="sxs-lookup"><span data-stu-id="4c401-160">Template Example</span></span>

<span data-ttu-id="4c401-161">L’exemple suivant montre un exemple de modèle.</span><span class="sxs-lookup"><span data-stu-id="4c401-161">The following shows an example template.</span></span>


```
template Mesh {
<3D82AB44-62DA-11cf-AB39-0020AF71E433>
DWORD nVertices;
array Vector vertices[nVertices];
DWORD nFaces;
array MeshFace faces[nFaces];
 [ ... ]                // An open template
}
template Vector {
<3D82AB5E-62DA-11cf-AB39-0020AF71E433>
FLOAT x;
FLOAT y;
FLOAT z;
}                        // A closed template
template FileSystem {
<UUID>
STRING name;
[ Directory <UUID>, File <UUID> ]    // A restricted template
}
```



## <a name="related-topics"></a><span data-ttu-id="4c401-162">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4c401-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c401-163">Encodage de texte</span><span class="sxs-lookup"><span data-stu-id="4c401-163">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



