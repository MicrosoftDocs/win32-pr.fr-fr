---
title: Fichiers générés pour une interface COM
description: Pour les interfaces COM, le compilateur MIDL combine toutes les données et routines auxiliaires du serveur d’objets et du client en un seul fichier proxy d’interface.
ms.assetid: 13063ee8-cb41-48a7-b90b-ea08c19c5230
keywords:
- Compilateur MIDL MIDL, MIDL et COM
- MIDL COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ea38ef85baa03890e323b4ba9d5eae4f295429
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940915"
---
# <a name="files-generated-for-a-com-interface"></a><span data-ttu-id="1b4f6-105">Fichiers générés pour une interface COM</span><span class="sxs-lookup"><span data-stu-id="1b4f6-105">Files Generated for a COM Interface</span></span>

<span data-ttu-id="1b4f6-106">Pour les interfaces COM, le compilateur MIDL combine toutes les données et routines auxiliaires du serveur d’objets et du client en un seul fichier proxy d’interface.</span><span class="sxs-lookup"><span data-stu-id="1b4f6-106">For COM interfaces, the MIDL compiler combines all client and object server auxiliary routines and data into a single interface proxy file.</span></span> <span data-ttu-id="1b4f6-107">Ce fichier comprend des points d’entrée de substitution pour les clients et les serveurs.</span><span class="sxs-lookup"><span data-stu-id="1b4f6-107">This file includes the surrogate entry points for both clients and servers.</span></span> <span data-ttu-id="1b4f6-108">En outre, le compilateur MIDL génère un fichier d’en-tête d’interface, un fichier UUID d’interface et un fichier d’inscription d’interface.</span><span class="sxs-lookup"><span data-stu-id="1b4f6-108">In addition, the MIDL compiler generates an interface header file, an interface UUID file and an interface registration file.</span></span> <span data-ttu-id="1b4f6-109">Vous allez utiliser tous ces fichiers lors de la création d’une DLL de proxy qui contient le code pour prendre en charge l’utilisation de l’interface par les applications clientes et les serveurs d’objets.</span><span class="sxs-lookup"><span data-stu-id="1b4f6-109">You will use all these files when creating a proxy DLL that contains the code to support the use of the interface by both client applications and object servers.</span></span> <span data-ttu-id="1b4f6-110">Vous allez également utiliser le fichier d’en-tête d’interface et le fichier UUID de l’interface lors de la création du fichier exécutable pour une application cliente qui utilise l’interface.</span><span class="sxs-lookup"><span data-stu-id="1b4f6-110">You will also use the interface header file and the interface UUID file when creating the executable file for a client application that uses the interface.</span></span>

<span data-ttu-id="1b4f6-111">Les rubriques suivantes décrivent chacun des fichiers générés pour une interface COM personnalisée, que vous identifiez en incluant l’attribut d' **\[** [**objet**](object.md) **\]** dans la liste des attributs d’interface du fichier IDL :</span><span class="sxs-lookup"><span data-stu-id="1b4f6-111">The following topics describe each of the files generated for a custom COM interface, which you identify by including the **\[**[**object**](object.md)**\]** attribute in the interface attribute list of the IDL file:</span></span>

-   [<span data-ttu-id="1b4f6-112">Fichier de proxy d’interface</span><span class="sxs-lookup"><span data-stu-id="1b4f6-112">The Interface Proxy File</span></span>](the-interface-proxy-file.md)
-   [<span data-ttu-id="1b4f6-113">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="1b4f6-113">The Header Files</span></span>](the-header-files.md)
-   [<span data-ttu-id="1b4f6-114">Fichier UUID de l’interface</span><span class="sxs-lookup"><span data-stu-id="1b4f6-114">The Interface UUID File</span></span>](the-interface-uuid-file.md)
-   [<span data-ttu-id="1b4f6-115">Fichier d’inscription de l’interface</span><span class="sxs-lookup"><span data-stu-id="1b4f6-115">The Interface Registration File</span></span>](the-interface-registration-file.md)

<span data-ttu-id="1b4f6-116">Pour plus d’informations, consultez [fichier de configuration d’application (ACF)](application-configuration-file-acf-.md), [**\_ configuration/App**](-app-config.md), [fichier de définition d’interface (IDL)](interface-definition-idl-file.md)et [génération et inscription d’une dll proxy](../com/building-and-registering-a-proxy-dll.md).</span><span class="sxs-lookup"><span data-stu-id="1b4f6-116">For more information, see [Application Configuration File (ACF)](application-configuration-file-acf-.md), [**/app\_config**](-app-config.md), [Interface Definition (IDL) File](interface-definition-idl-file.md), and [Building and Registering a Proxy DLL](../com/building-and-registering-a-proxy-dll.md).</span></span>

 

 