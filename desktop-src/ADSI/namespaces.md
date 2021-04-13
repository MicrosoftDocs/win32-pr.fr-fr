---
title: Espaces de noms
description: Les objets qui résident dans un espace de noms donné sont identifiés par un nom unique.
ms.assetid: d42b4b18-d38f-4071-8e3e-9b9b71d46d4b
ms.tgt_platform: multiple
keywords:
- espaces de noms ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29d93963b2fc2b3fa6ea0eb486fe95b46ba0e9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379591"
---
# <a name="namespaces"></a><span data-ttu-id="dfe8f-104">Espaces de noms</span><span class="sxs-lookup"><span data-stu-id="dfe8f-104">Namespaces</span></span>

<span data-ttu-id="dfe8f-105">Les objets qui résident dans un espace de noms donné sont identifiés par un nom unique.</span><span class="sxs-lookup"><span data-stu-id="dfe8f-105">Objects that reside within a given namespace are identified by a unique name.</span></span> <span data-ttu-id="dfe8f-106">Par exemple, les fichiers stockés sur un lecteur de disque PC résident dans l’espace de noms du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="dfe8f-106">For example, files stored on a PC disk drive reside in the file system namespace.</span></span> <span data-ttu-id="dfe8f-107">Le nom unique d’un fichier est basé sur l’emplacement où il est stocké dans l’espace de noms du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="dfe8f-107">The unique name of a file is based on where it is stored in the file system namespace.</span></span> <span data-ttu-id="dfe8f-108">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="dfe8f-108">For example:</span></span>


```C++
C:\public\documents\adsi\adsi_spec.doc
```



<span data-ttu-id="dfe8f-109">Les espaces de noms de service d’annuaire identifient également les objets qu’ils contiennent par des noms uniques qui sont généralement basés sur l’emplacement dans le répertoire où se trouve l’objet.</span><span class="sxs-lookup"><span data-stu-id="dfe8f-109">Directory service namespaces also identify the objects they contain by unique names which are usually based on the location in the directory where the object can be found.</span></span> <span data-ttu-id="dfe8f-110">Par exemple, dans un répertoire X. 500, un objet donné peut avoir un nom semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="dfe8f-110">For example, in an X.500 directory, a given object might have a name like this:</span></span>


```C++
CN=John,OU=Marketing,O=Fabrikam
```



<span data-ttu-id="dfe8f-111">Différents services d’annuaire utilisent des formes différentes pour nommer les objets qu’ils contiennent.</span><span class="sxs-lookup"><span data-stu-id="dfe8f-111">Different directory services use different forms for naming the objects they contain.</span></span> <span data-ttu-id="dfe8f-112">Cela complique le traitement de différents espaces de noms, en particulier pour les développeurs, en tenant compte de tous les environnements sur lesquels le code est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="dfe8f-112">This makes dealing with different namespaces challenging, especially for developers, considering all of the different environments on which the code might be running.</span></span>

<span data-ttu-id="dfe8f-113">L’un des objectifs de l’interface ADSI (Active Directory Service Interfaces) est de fournir une infrastructure d’attribution de noms qui permet d’accéder aux espaces de noms de différents fournisseurs de services d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="dfe8f-113">A goal of Active Directory Service Interfaces (ADSI) is to provide a naming framework that allows access to namespaces of different directory service providers.</span></span>

<span data-ttu-id="dfe8f-114">ADSI définit une convention d’affectation de noms qui permet d’identifier de manière unique un objet dans un environnement hétérogène.</span><span class="sxs-lookup"><span data-stu-id="dfe8f-114">ADSI defines a naming convention that can uniquely identify an object in a heterogeneous environment.</span></span> <span data-ttu-id="dfe8f-115">Ces noms sont appelés chaînes ADsPath.</span><span class="sxs-lookup"><span data-stu-id="dfe8f-115">These names are called ADsPath strings.</span></span> <span data-ttu-id="dfe8f-116">Les chaînes ADsPath prennent plusieurs formes :</span><span class="sxs-lookup"><span data-stu-id="dfe8f-116">ADsPath strings take several forms:</span></span>


```C++
"ADs://"
 
"LDAP://"
 
"WinNT://"
```



<span data-ttu-id="dfe8f-117">Des formats ADsPath supplémentaires peuvent être introduits par différents fournisseurs ADSI (tels que le fournisseur ADSI pour le serveur Internet Information Services, qui prend en charge le ADsPaths « IIS:// »).</span><span class="sxs-lookup"><span data-stu-id="dfe8f-117">Additional ADsPath formats can be introduced by different ADSI providers (such as the ADSI provider for the Internet Information Services server, which support the "IIS://" ADsPaths).</span></span>

 

 




