---
title: Ressource User-Defined
description: Une instruction de définition de ressource définie par l’utilisateur définit une ressource qui contient des données spécifiques à l’application.
ms.assetid: b1cfec71-5733-4900-97f6-c1cbb350c728
keywords:
- ressource définie par l’utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 909352c7f0643ed67b1d199fafba1ac8f15d2a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196708"
---
# <a name="user-defined-resource"></a><span data-ttu-id="a41e8-104">Ressource User-Defined</span><span class="sxs-lookup"><span data-stu-id="a41e8-104">User-Defined Resource</span></span>

<span data-ttu-id="a41e8-105">Une instruction de définition de ressource définie par l’utilisateur définit une ressource qui contient des données spécifiques à l’application.</span><span class="sxs-lookup"><span data-stu-id="a41e8-105">A user-defined resource-definition statement defines a resource that contains application-specific data.</span></span> <span data-ttu-id="a41e8-106">Les données peuvent avoir n’importe quel format et peuvent être définies en tant que contenu d’un fichier donné (si le paramètre de *nom de fichier* est donné) ou sous la forme d’une série de nombres et de chaînes (si le bloc de *données brutes* est spécifié).</span><span class="sxs-lookup"><span data-stu-id="a41e8-106">The data can have any format and can be defined either as the content of a given file (if the *filename* parameter is given) or as a series of numbers and strings (if the *raw-data* block is specified).</span></span>

``` syntax
nameID typeID filename
```

<span data-ttu-id="a41e8-107">Le *nom de fichier spécifie* le nom d’un fichier contenant les données binaires de la ressource.</span><span class="sxs-lookup"><span data-stu-id="a41e8-107">The *filename* specifies the name of a file containing the binary data of the resource.</span></span> <span data-ttu-id="a41e8-108">Le contenu du fichier est inclus en tant que ressource.</span><span class="sxs-lookup"><span data-stu-id="a41e8-108">The contents of the file are included as the resource.</span></span> <span data-ttu-id="a41e8-109">RC n’interprète pas les données binaires de quelque manière que ce soit.</span><span class="sxs-lookup"><span data-stu-id="a41e8-109">RC does not interpret the binary data in any way.</span></span> <span data-ttu-id="a41e8-110">Il incombe au programmeur de s’assurer que les données sont correctement alignées pour l’architecture de l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="a41e8-110">It is the programmer's responsibility to ensure that the data is properly aligned for the target computer architecture.</span></span>

<span data-ttu-id="a41e8-111">Une ressource définie par l’utilisateur peut également être entièrement définie dans le script de ressources à l’aide de la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="a41e8-111">A user-defined resource can also be defined completely in the resource script using the following syntax:</span></span>

``` syntax
nameID typeID  {  raw-data  }
```

## <a name="parameters"></a><span data-ttu-id="a41e8-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a41e8-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a41e8-113"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="a41e8-113"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="a41e8-114">Nom unique ou entier 16 bits non signé qui identifie la ressource.</span><span class="sxs-lookup"><span data-stu-id="a41e8-114">Unique name or a 16-bit unsigned integer that identifies the resource.</span></span>

</dd> <dt>

<span data-ttu-id="a41e8-115"><span id="typeID"></span><span id="typeid"></span><span id="TYPEID"></span>*typeID*</span><span class="sxs-lookup"><span data-stu-id="a41e8-115"><span id="typeID"></span><span id="typeid"></span><span id="TYPEID"></span>*typeID*</span></span>
</dt> <dd>

<span data-ttu-id="a41e8-116">Nom unique ou entier 16 bits non signé qui identifie le type de ressource.</span><span class="sxs-lookup"><span data-stu-id="a41e8-116">Unique name or a 16-bit unsigned integer that identifies the resource type.</span></span> <span data-ttu-id="a41e8-117">Si un nombre est donné, il doit être supérieur à 255.</span><span class="sxs-lookup"><span data-stu-id="a41e8-117">If a number is given, it must be greater than 255.</span></span> <span data-ttu-id="a41e8-118">Les nombres 1 à 255 sont réservés pour les types de ressources redéfinis existants et futurs.</span><span class="sxs-lookup"><span data-stu-id="a41e8-118">The numbers 1 through 255 are reserved for existing and future redefined resource types.</span></span>

</dd> <dt>

<span data-ttu-id="a41e8-119"><span id="filename"></span><span id="FILENAME"></span>*extension*</span><span class="sxs-lookup"><span data-stu-id="a41e8-119"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="a41e8-120">Nom du fichier qui contient les données de ressource.</span><span class="sxs-lookup"><span data-stu-id="a41e8-120">Name of the file that contains the resource data.</span></span> <span data-ttu-id="a41e8-121">Le paramètre doit être un nom de fichier valide ; il doit s’agir d’un chemin d’accès complet si le fichier ne se trouve pas dans le répertoire de travail actuel.</span><span class="sxs-lookup"><span data-stu-id="a41e8-121">The parameter must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span>

</dd> <dt>

<span data-ttu-id="a41e8-122"><span id="raw-data"></span><span id="RAW-DATA"></span>*données brutes*</span><span class="sxs-lookup"><span data-stu-id="a41e8-122"><span id="raw-data"></span><span id="RAW-DATA"></span>*raw-data*</span></span>
</dt> <dd>

<span data-ttu-id="a41e8-123">Données brutes constituées d’un ou plusieurs entiers ou chaînes de caractères.</span><span class="sxs-lookup"><span data-stu-id="a41e8-123">Raw data consisting of one or more integers or strings of characters.</span></span> <span data-ttu-id="a41e8-124">Les entiers peuvent être spécifiés au format décimal, octal ou hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="a41e8-124">Integers can be specified in decimal, octal, or hexadecimal format.</span></span> <span data-ttu-id="a41e8-125">Pour être compatible avec Windows 16 bits, les entiers sont stockés sous la forme de valeurs WORD.</span><span class="sxs-lookup"><span data-stu-id="a41e8-125">To be compatible with 16-bit Windows, integers are stored as WORD values.</span></span> <span data-ttu-id="a41e8-126">Vous pouvez stocker un entier comme valeur DWORD en qualifiant l’entier avec le suffixe « L ».</span><span class="sxs-lookup"><span data-stu-id="a41e8-126">You can store an integer as a DWORD value by qualifying the integer with the "L" suffix.</span></span>

<span data-ttu-id="a41e8-127">Les chaînes sont placées entre guillemets.</span><span class="sxs-lookup"><span data-stu-id="a41e8-127">Strings are enclosed in quotation marks.</span></span> <span data-ttu-id="a41e8-128">RC n’ajoute pas automatiquement un caractère null de fin à une chaîne.</span><span class="sxs-lookup"><span data-stu-id="a41e8-128">RC does not automatically append a terminating null character to a string.</span></span> <span data-ttu-id="a41e8-129">Chaque chaîne est une séquence de caractères ANSI spécifiée, sauf si vous la qualifiez comme une chaîne de caractères larges avec le préfixe « L ».</span><span class="sxs-lookup"><span data-stu-id="a41e8-129">Each string is a sequence of the specified ANSI characters, unless you qualify it as a wide-character string with the "L" prefix.</span></span>

<span data-ttu-id="a41e8-130">Le bloc de données commence sur une limite **DWORD** et RC n’effectue aucun remplissage ou alignement des données dans le bloc de *données brutes* .</span><span class="sxs-lookup"><span data-stu-id="a41e8-130">The block of data begins on a **DWORD** boundary and RC performs no padding or alignment of data within the *raw-data* block.</span></span> <span data-ttu-id="a41e8-131">Il incombe au programmeur de garantir l’alignement correct des données dans le bloc.</span><span class="sxs-lookup"><span data-stu-id="a41e8-131">It is the programmer's responsibility to ensure the proper alignment of data within the block.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="a41e8-132">Exemple</span><span class="sxs-lookup"><span data-stu-id="a41e8-132">Example</span></span>

<span data-ttu-id="a41e8-133">L’exemple suivant illustre plusieurs instructions définies par l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="a41e8-133">The following example shows several user-defined statements:</span></span>

``` syntax
array   MYRES   data.res
14      300     custom.res
18 MYRES2
{
   "Here is an ANSI string\0",    // explicitly null-terminated 
   L"Here is a Unicode string\0", // explicitly null-terminated 
   1024,                          // integer, stored as WORD 
   7L,                            // integer, stored as DWORD 
   0x029a,                        // hex integer 
   0o733,                         // octal integer 
}
```

 

 




