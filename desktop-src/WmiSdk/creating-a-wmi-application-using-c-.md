---
description: 'Pour créer une application pour WMI à l’aide de C++ : vous devez initialiser COM, accéder aux protocoles WMI et les définir, et effectuer un nettoyage manuel.'
ms.assetid: 0b9b7990-6982-4ba9-8dba-7470990405f7
ms.tgt_platform: multiple
title: Création d’une application WMI à l’aide de C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baaa4f7e79828b2cb6cb496254d906182ff611ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320338"
---
# <a name="creating-a-wmi-application-using-c"></a><span data-ttu-id="efa5b-103">Création d’une application WMI à l’aide de C++</span><span class="sxs-lookup"><span data-stu-id="efa5b-103">Creating a WMI Application Using C++</span></span>

<span data-ttu-id="efa5b-104">Pour créer une application pour WMI à l’aide de C++ : vous devez initialiser COM, accéder aux protocoles WMI et les définir, et effectuer un nettoyage manuel.</span><span class="sxs-lookup"><span data-stu-id="efa5b-104">To create an application for WMI using C++: you must initialize COM, access and set WMI protocols, and perform a manual cleanup.</span></span> <span data-ttu-id="efa5b-105">Toutefois, C++ présente l’avantage de la flexibilité et de la puissance.</span><span class="sxs-lookup"><span data-stu-id="efa5b-105">However, C++ does have the advantage of flexibility and power.</span></span> <span data-ttu-id="efa5b-106">Par conséquent, bien que vous soyez mieux servi à utiliser Visual Basic Scripting Edition (VBScript) ou Windows PowerShell pour des processus simples, C++ fonctionne mieux pour des applications plus sophistiquées et est nécessaire pour écrire des [fournisseurs](providing-data-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="efa5b-106">Therefore, while you are better served in using Visual Basic Scripting Edition (VBScript) or Windows PowerShell for simple processes, C++ works better for more sophisticated applications and is required for writing [providers](providing-data-to-wmi.md).</span></span>

<span data-ttu-id="efa5b-107">La procédure suivante décrit comment créer une application WMI.</span><span class="sxs-lookup"><span data-stu-id="efa5b-107">The following procedure describes how to create a WMI application.</span></span>

<span data-ttu-id="efa5b-108">**Pour créer une application WMI**</span><span class="sxs-lookup"><span data-stu-id="efa5b-108">**To create a WMI application**</span></span>

1.  <span data-ttu-id="efa5b-109">[Initialisez com](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="efa5b-109">[Initialize COM](initializing-com-for-a-wmi-application.md).</span></span>

    <span data-ttu-id="efa5b-110">Étant donné que WMI est basé sur la technologie COM, vous devez effectuer des appels aux fonctions [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) et [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) pour accéder à WMI.</span><span class="sxs-lookup"><span data-stu-id="efa5b-110">Because WMI is based on COM technology, you must perform calls to the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) functions to access WMI.</span></span>

2.  <span data-ttu-id="efa5b-111">[Créer une connexion à un espace de noms WMI](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="efa5b-111">[Create a connection to a WMI namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

    <span data-ttu-id="efa5b-112">Par définition, WMI s’exécute dans un processus différent de celui de votre application.</span><span class="sxs-lookup"><span data-stu-id="efa5b-112">By definition, WMI runs in a different process than your application.</span></span> <span data-ttu-id="efa5b-113">Par conséquent, vous devez créer une connexion entre votre application et WMI.</span><span class="sxs-lookup"><span data-stu-id="efa5b-113">Therefore, you must create a connection between your application and WMI.</span></span>

3.  <span data-ttu-id="efa5b-114">[Définissez les niveaux de sécurité sur la connexion WMI](setting-the-security-levels-on-a-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="efa5b-114">[Set the security levels on the WMI connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

    <span data-ttu-id="efa5b-115">Pour utiliser la connexion que vous créez à WMI, vous devez définir les niveaux d’emprunt d’identité et d’authentification pour votre application.</span><span class="sxs-lookup"><span data-stu-id="efa5b-115">To use the connection you create to WMI, you must set the impersonation and authentication levels for your application.</span></span>

4.  <span data-ttu-id="efa5b-116">Implémentez le rôle de votre application.</span><span class="sxs-lookup"><span data-stu-id="efa5b-116">Implement the purpose of your application.</span></span>

    <span data-ttu-id="efa5b-117">WMI expose une variété d’interfaces COM qui permettent d’accéder aux données et de les manipuler au sein de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="efa5b-117">WMI exposes a variety of COM interfaces use to access and manipulate data across your enterprise.</span></span> <span data-ttu-id="efa5b-118">Pour plus d’informations, consultez [manipulation d’informations de classes et d’instances](manipulating-class-and-instance-information.md), [réception d’un événement WMI](receiving-a-wmi-event.md)et [de l’API com pour WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="efa5b-118">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), [Receiving a WMI Event](receiving-a-wmi-event.md), and [COM API for WMI](com-api-for-wmi.md).</span></span>

    <span data-ttu-id="efa5b-119">C’est là que la majeure partie de votre application cliente WMI doit exister, comme l’accès aux objets WMI ou la manipulation des données.</span><span class="sxs-lookup"><span data-stu-id="efa5b-119">This is where the bulk of your WMI client application should exist, such as accessing WMI objects or manipulating data.</span></span>

5.  <span data-ttu-id="efa5b-120">[Nettoyez et arrêtez votre application](cleaning-up-and-shutting-down-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="efa5b-120">[Cleanup and shut down your application](cleaning-up-and-shutting-down-a-wmi-application.md).</span></span>

    <span data-ttu-id="efa5b-121">Une fois que vous avez terminé vos requêtes dans WMI, vous devez détruire tous les pointeurs COM et arrêter correctement votre application.</span><span class="sxs-lookup"><span data-stu-id="efa5b-121">After you complete your queries to WMI, you should destroy all COM pointers and shut down your application correctly.</span></span>

<span data-ttu-id="efa5b-122">Pour plus d’informations et pour obtenir un exemple de code sur la création d’une application WMI, consultez [exemple : création d’une application WMI](example-creating-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="efa5b-122">For more information and a code example about how to create a WMI application, see [Example: Creating a WMI Application](example-creating-a-wmi-application.md).</span></span>

 

 
