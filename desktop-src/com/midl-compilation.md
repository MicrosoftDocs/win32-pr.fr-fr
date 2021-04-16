---
title: Compilation MIDL
description: Compilation MIDL
ms.assetid: 2797ee3b-82fd-4cb5-9e95-23b2f2a8f011
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e281fa66ec1b8f997dd58fc55a67c19a801d2d36
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463758"
---
# <a name="midl-compilation"></a><span data-ttu-id="83a19-103">Compilation MIDL</span><span class="sxs-lookup"><span data-stu-id="83a19-103">MIDL Compilation</span></span>

<span data-ttu-id="83a19-104">À partir d’un fichier IDL, tel que [example2. idl](anatomy-of-an-idl-file.md), qui définit une ou plusieurs interfaces com et une bibliothèque de types, le compilateur MIDL (Midl.exe) génère les fichiers décrits dans le tableau suivant comme sortie par défaut.</span><span class="sxs-lookup"><span data-stu-id="83a19-104">Given an IDL file, such as [Example2.idl](anatomy-of-an-idl-file.md), that defines one or more COM interfaces and a type library, the MIDL compiler (Midl.exe) generates the files described in the following table as the default output.</span></span>



| <span data-ttu-id="83a19-105">Nom de fichier</span><span class="sxs-lookup"><span data-stu-id="83a19-105">Filename</span></span>                 | <span data-ttu-id="83a19-106">Description</span><span class="sxs-lookup"><span data-stu-id="83a19-106">Description</span></span>                                                                                                                                                                                           |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83a19-107">Example2. h</span><span class="sxs-lookup"><span data-stu-id="83a19-107">Example2.h</span></span><br/>    | <span data-ttu-id="83a19-108">Fichier d’en-tête, contenant les définitions de type et les déclarations de fonction pour toutes les interfaces définies dans le fichier IDL, ainsi que les déclarations anticipées pour les routines que les stubs appellent.</span><span class="sxs-lookup"><span data-stu-id="83a19-108">The header file, containing type definitions and function declarations for all of the interfaces defined in the IDL file as well as forward declarations for routines that the stubs call.</span></span><br/> |
| <span data-ttu-id="83a19-109">Example2 \_ p. c</span><span class="sxs-lookup"><span data-stu-id="83a19-109">Example2\_p.c</span></span><br/> | <span data-ttu-id="83a19-110">Le fichier proxy/stub, qui comprend les points d’entrée de substitution pour les clients et pour les serveurs.</span><span class="sxs-lookup"><span data-stu-id="83a19-110">The proxy/stub file, which includes the surrogate entry points both for clients and for servers.</span></span><br/>                                                                                           |
| <span data-ttu-id="83a19-111">Example2 \_ i. c</span><span class="sxs-lookup"><span data-stu-id="83a19-111">Example2\_i.c</span></span><br/> | <span data-ttu-id="83a19-112">Le fichier d’ID d’interface, qui définit le GUID pour chaque interface spécifiée dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="83a19-112">The interface ID file, which defines the GUID for every interface specified in the IDL file.</span></span><br/>                                                                                               |
| <span data-ttu-id="83a19-113">Example2. tlb</span><span class="sxs-lookup"><span data-stu-id="83a19-113">Example2.tlb</span></span><br/>  | <span data-ttu-id="83a19-114">Fichier de document composé qui contient des informations sur les types et les objets.</span><span class="sxs-lookup"><span data-stu-id="83a19-114">A compound document file that contains information about types and objects.</span></span><br/>                                                                                                                |
| <span data-ttu-id="83a19-115">Dlldata. c</span><span class="sxs-lookup"><span data-stu-id="83a19-115">Dlldata.c</span></span><br/>     | <span data-ttu-id="83a19-116">Contient les données dont vous avez besoin pour créer une DLL de proxy/stub.</span><span class="sxs-lookup"><span data-stu-id="83a19-116">Contains the data you need to create a proxy/stub DLL.</span></span><br/>                                                                                                                                     |



 

<span data-ttu-id="83a19-117">Vous utilisez le fichier d’en-tête et tous les fichiers. c pour [créer une dll de proxy](building-and-registering-a-proxy-dll.md) pouvant prendre en charge l’interface lorsqu’elle est utilisée à la fois par les applications clientes et par les serveurs d’objets.</span><span class="sxs-lookup"><span data-stu-id="83a19-117">You use the header file and all of the .c files to [create a proxy DLL](building-and-registering-a-proxy-dll.md) that can support the interface when used both by client applications and by object servers.</span></span> <span data-ttu-id="83a19-118">Vous utilisez le fichier d’en-tête d’interface (example2. h) et le \_ fichier d’ID d’interface (example2 i. c) lors de la création du fichier exécutable pour une application cliente qui utilise l’interface.</span><span class="sxs-lookup"><span data-stu-id="83a19-118">You use the interface header file (Example2.h) and the interface ID (Example2\_i.c) file when creating the executable file for a client application that uses the interface.</span></span> <span data-ttu-id="83a19-119">Vous pouvez choisir d’inclure le fichier de bibliothèque de types en tant que ressource dans votre fichier EXE ou DLL, ou vous pouvez l’envoyer en tant que fichier distinct.</span><span class="sxs-lookup"><span data-stu-id="83a19-119">You can choose to include the type library file as a resource in your EXE or DLL, or you can ship it as a separate file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83a19-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="83a19-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83a19-121">Fichiers générés pour une interface COM</span><span class="sxs-lookup"><span data-stu-id="83a19-121">Files Generated for a COM Interface</span></span>](/windows/desktop/Midl/files-generated-for-a-com-interface)
</dt> <dt>

[<span data-ttu-id="83a19-122">Options du compilateur MIDL</span><span class="sxs-lookup"><span data-stu-id="83a19-122">MIDL Compiler Options</span></span>](midl-compiler-options.md)
</dt> </dl>

 

