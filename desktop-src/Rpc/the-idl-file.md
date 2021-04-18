---
title: Fichier IDL
description: Le fichier IDL se compose d’une ou de plusieurs définitions d’interface, chacune ayant un en-tête et un corps.
ms.assetid: 64a30a12-a53e-4c53-b8cf-7af85ffd0a94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862adfad2a43f10dac3598279554fd6e1f00a302
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463234"
---
# <a name="the-idl-file"></a><span data-ttu-id="176b2-103">Fichier IDL</span><span class="sxs-lookup"><span data-stu-id="176b2-103">The IDL File</span></span>

<span data-ttu-id="176b2-104">Le fichier IDL se compose d’une ou de plusieurs définitions d’interface, chacune ayant un en-tête et un corps.</span><span class="sxs-lookup"><span data-stu-id="176b2-104">The IDL file consists of one or more interface definitions, each of which has a header and a body.</span></span> <span data-ttu-id="176b2-105">L’en-tête contient des informations qui s’appliquent à l’ensemble de l’interface, telles que l’UUID.</span><span class="sxs-lookup"><span data-stu-id="176b2-105">The header contains information that applies to the entire interface, such as the UUID.</span></span> <span data-ttu-id="176b2-106">Ces informations sont placées entre crochets et sont suivies de l' **interface** du mot clé et du nom de l’interface.</span><span class="sxs-lookup"><span data-stu-id="176b2-106">This information is enclosed in square brackets and is followed by the keyword **interface** and the interface name.</span></span> <span data-ttu-id="176b2-107">Le corps contient des définitions de type de données de style C et des prototypes de fonction, complétés par des attributs qui décrivent comment les données sont transmises sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="176b2-107">The body contains C-style data type definitions and function prototypes, augmented with attributes that describe how the data is transmitted over the network.</span></span>

<span data-ttu-id="176b2-108">Dans cet exemple, l’en-tête d’interface contient uniquement l’UUID et le numéro de version.</span><span class="sxs-lookup"><span data-stu-id="176b2-108">In this example, the interface header contains only the UUID and the version number.</span></span> <span data-ttu-id="176b2-109">Le numéro de version garantit qu’en présence de plusieurs versions d’une interface RPC, seules les versions compatibles du client et du serveur seront connectées.</span><span class="sxs-lookup"><span data-stu-id="176b2-109">The version number ensures that when there are multiple versions of an RPC interface, only compatible versions of the client and server will be connected.</span></span>

<span data-ttu-id="176b2-110">Le corps de l’interface contient le prototype de fonction pour **HelloProc**.</span><span class="sxs-lookup"><span data-stu-id="176b2-110">The interface body contains the function prototype for **HelloProc**.</span></span> <span data-ttu-id="176b2-111">Dans ce prototype, le paramètre de fonction pszString a les attributs **\[** [**dans**](/windows/desktop/Midl/in) **\]** et **\[** [**String**](/windows/desktop/Midl/string) **\]** .</span><span class="sxs-lookup"><span data-stu-id="176b2-111">In this prototype, the function parameter pszString has the attributes **\[**[**in**](/windows/desktop/Midl/in)**\]** and **\[**[**string**](/windows/desktop/Midl/string)**\]**.</span></span> <span data-ttu-id="176b2-112">L’attribut **\[ in \]** indique à la bibliothèque Runtime que le paramètre est passé uniquement du client au serveur.</span><span class="sxs-lookup"><span data-stu-id="176b2-112">The **\[in\]** attribute tells the run-time library that the parameter is passed only from the client to the server.</span></span> <span data-ttu-id="176b2-113">L’attribut **\[ String \]** spécifie que le stub doit traiter le paramètre comme une chaîne de caractères de style C.</span><span class="sxs-lookup"><span data-stu-id="176b2-113">The **\[string\]** attribute specifies that the stub should treat the parameter as a C-style character string.</span></span>

<span data-ttu-id="176b2-114">L’application cliente doit être en mesure d’arrêter l’application serveur. par conséquent, l’interface contient un prototype pour une autre fonction à distance,**Shutdown** , qui sera implémentée plus tard dans ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="176b2-114">The client application should be able to shut down the server application, so the interface contains a prototype for another remote function,**Shutdown** , that will be implemented later in this tutorial.</span></span>

``` syntax
//file hello.idl
[
    uuid(7a98c250-6808-11cf-b73b-00aa00b677a7),
    version(1.0)
]
interface hello
{
    void HelloProc([in, string] unsigned char * pszString);
    void Shutdown(void);
}
```

 

 