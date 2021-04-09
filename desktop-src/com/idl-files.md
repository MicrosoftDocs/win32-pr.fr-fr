---
title: Fichiers IDL
description: Fichiers IDL
ms.assetid: 94a6752d-fcf3-47ce-ac3f-be1d1c9768e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bc9a736bf9b9a77ec1cb655fb5c76e9e1c0d27e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842781"
---
# <a name="idl-files"></a><span data-ttu-id="d293d-103">Fichiers IDL</span><span class="sxs-lookup"><span data-stu-id="d293d-103">IDL Files</span></span>

<span data-ttu-id="d293d-104">COM utilise le Microsoft Interface Definition Language (MIDL) pour décrire les objets COM.</span><span class="sxs-lookup"><span data-stu-id="d293d-104">COM uses the Microsoft Interface Definition Language (MIDL) to describe COM objects.</span></span> <span data-ttu-id="d293d-105">MIDL est une extension de l’IDL pour les environnements informatiques distribués définis par Open Software Foundation, qui a été développé pour définir les interfaces des appels de procédure distante dans les applications client/serveur traditionnelles.</span><span class="sxs-lookup"><span data-stu-id="d293d-105">MIDL is an extension of the IDL for distributed computing environments defined by the Open Software Foundation, which was developed to define interfaces for remote procedure calls in traditional client/server applications.</span></span> <span data-ttu-id="d293d-106">MIDL comprend la plupart des attributs et des instructions du langage ODL (Object Definition Language), le langage utilisé à l’origine pour générer des bibliothèques de types pour OLE Automation.</span><span class="sxs-lookup"><span data-stu-id="d293d-106">MIDL includes most of the attributes and statements of Object Definition Language (ODL), the language originally used to generate type libraries for OLE Automation.</span></span>

<span data-ttu-id="d293d-107">En C++ et Java, un développeur créant un objet COM crée un fichier IDL que le compilateur MIDL traite ensuite pour créer une bibliothèque de types ou des fichiers d’en-tête et de proxy, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="d293d-107">In C++ and Java, a developer building a COM object creates an IDL file that the MIDL compiler then processes to create a type library or header and proxy files, or both.</span></span> <span data-ttu-id="d293d-108">Une *bibliothèque de types* est un fichier binaire qui décrit l’objet com ou les interfaces com, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="d293d-108">A *type library* is a binary file that describes the COM object or COM interfaces, or both.</span></span> <span data-ttu-id="d293d-109">Une bibliothèque de types est la version compilée du fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="d293d-109">A type library is the compiled version of the IDL file.</span></span> <span data-ttu-id="d293d-110">Toutefois, les bibliothèques de types prennent uniquement en charge la sémantique ODL.</span><span class="sxs-lookup"><span data-stu-id="d293d-110">However, type libraries support ODL semantics only.</span></span> <span data-ttu-id="d293d-111">En particulier, ils ne peuvent pas représenter toutes les informations d’un fichier IDL lié aux attributs IDL, par exemple la \[ [**taille \_ est**](/windows/desktop/Midl/size-is) \] .</span><span class="sxs-lookup"><span data-stu-id="d293d-111">In particular, they cannot represent all the information from an IDL file related to IDL attributes like \[[**size\_is**](/windows/desktop/Midl/size-is)\].</span></span> <span data-ttu-id="d293d-112">Vous devez créer et utiliser des fichiers de proxy pour les fichiers IDL affectés par la perte d’informations dans la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="d293d-112">You need to create and use proxy files for IDL files affected by information loss in the type library.</span></span>

<span data-ttu-id="d293d-113">Dans Visual Basic, un développeur qui crée un objet COM ne crée pas de fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="d293d-113">In Visual Basic, a developer creating a COM object does not create an IDL file.</span></span> <span data-ttu-id="d293d-114">Au lieu de cela, Visual Basic recueille des informations à l’aide des propriétés de classe et de projet et crée directement la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="d293d-114">Instead, Visual Basic gathers information using class and project properties and directly creates the type library.</span></span>

 

 