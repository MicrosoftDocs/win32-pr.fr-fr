---
title: Fichier de définition d’interface (IDL)
description: Par Convention, le fichier qui contient les définitions d’interface et de bibliothèque de types est appelé fichier IDL et a une extension de nom de fichier. idl.
ms.assetid: 4df87df8-3206-4845-b5ab-d77ea443b9e3
keywords:
- interfaces MIDL, fichier IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950daa2c1841f6e4b3f015f14e373804fcd34b80
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725429"
---
# <a name="interface-definition-idl-file"></a><span data-ttu-id="78fb2-104">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="78fb2-104">Interface Definition (IDL) File</span></span>

<span data-ttu-id="78fb2-105">Par Convention, le fichier qui contient les définitions d’interface et de bibliothèque de types est appelé fichier IDL et a une extension de nom de fichier. idl.</span><span class="sxs-lookup"><span data-stu-id="78fb2-105">By convention, the file that contains interface and type library definitions is called an IDL file, and has an .idl file name extension.</span></span> <span data-ttu-id="78fb2-106">En réalité, le compilateur MIDL analyse un fichier de définition d’interface indépendamment de son extension.</span><span class="sxs-lookup"><span data-stu-id="78fb2-106">In reality, the MIDL compiler will parse an interface definition file regardless of its extension.</span></span> <span data-ttu-id="78fb2-107">Une interface est identifiée par l' [**interface**](interface.md)de mot clé.</span><span class="sxs-lookup"><span data-stu-id="78fb2-107">An interface is identified by the keyword [**interface**](interface.md).</span></span>

<span data-ttu-id="78fb2-108">Chaque interface se compose d’un en-tête et d’un corps.</span><span class="sxs-lookup"><span data-stu-id="78fb2-108">Each interface consists of a header and a body.</span></span> <span data-ttu-id="78fb2-109">L’en-tête d’interface contient des attributs qui s’appliquent à l’ensemble de l’interface.</span><span class="sxs-lookup"><span data-stu-id="78fb2-109">The interface header contains attributes that apply to the entire interface.</span></span> <span data-ttu-id="78fb2-110">Le corps de l’interface contient les définitions d’interface restantes.</span><span class="sxs-lookup"><span data-stu-id="78fb2-110">The body of the interface contains the remaining interface definitions.</span></span> <span data-ttu-id="78fb2-111">Pour obtenir une vue d’ensemble des interfaces et des fichiers IDL, consultez [le fichier IDL (Interface Definition Language)](/windows/desktop/Rpc/the-interface-definition-language-idl-file).</span><span class="sxs-lookup"><span data-stu-id="78fb2-111">For an overview of interfaces and IDL files, see [The Interface Definition Language (IDL) File](/windows/desktop/Rpc/the-interface-definition-language-idl-file).</span></span> <span data-ttu-id="78fb2-112">Pour obtenir un résumé des attributs qui peuvent être utilisés dans un en-tête d’interface, consultez [attributs IDL](idl-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="78fb2-112">For a summary of attributes that can be used in an interface header, see [IDL Attributes](idl-attributes.md).</span></span>

 

 