---
description: Un consommateur logique est une instance d’une classe de consommateur d’événements permanente.
ms.assetid: fd984de8-0fe6-4b32-8e8c-4e2db84b4cc0
ms.tgt_platform: multiple
title: Création d’un consommateur logique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dcbd62f2eee57a9e254d5700344d7b8da414469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520148"
---
# <a name="creating-a-logical-consumer"></a><span data-ttu-id="f3fba-103">Création d’un consommateur logique</span><span class="sxs-lookup"><span data-stu-id="f3fba-103">Creating a Logical Consumer</span></span>

<span data-ttu-id="f3fba-104">Un consommateur logique est une instance d’une classe de consommateur d’événements permanente.</span><span class="sxs-lookup"><span data-stu-id="f3fba-104">A logical consumer is an instance of a permanent event consumer class.</span></span> <span data-ttu-id="f3fba-105">L’objectif principal d’un consommateur logique est de fournir au consommateur physique les paramètres des activités effectuées par le consommateur physique.</span><span class="sxs-lookup"><span data-stu-id="f3fba-105">The main purpose of a logical consumer is to provide the physical consumer with the parameters for the activities the physical consumer performs.</span></span> <span data-ttu-id="f3fba-106">Pour plus d’informations, consultez [création d’une classe de consommateur d’événements permanent](creating-a-new-permanent-event-consumer-class.md).</span><span class="sxs-lookup"><span data-stu-id="f3fba-106">For more information, see [Creating a New Permanent Event Consumer Class](creating-a-new-permanent-event-consumer-class.md).</span></span> <span data-ttu-id="f3fba-107">Le consommateur permanent doit avoir le même [**CreatorSID**](--eventconsumer.md) dans les instances de consommateur, de filtre et de liaison.</span><span class="sxs-lookup"><span data-stu-id="f3fba-107">The permanent consumer must have the same [**CreatorSID**](--eventconsumer.md) in the consumer, filter, and binding instances.</span></span> <span data-ttu-id="f3fba-108">Pour plus d’informations, consultez [réception d’événements en toute sécurité](receiving-events-securely.md).</span><span class="sxs-lookup"><span data-stu-id="f3fba-108">For more information, see [Receiving Events Securely](receiving-events-securely.md).</span></span> <span data-ttu-id="f3fba-109">Pour obtenir un exemple d’utilisation d’un consommateur logique, consultez [exécution d’un script basé sur un événement](running-a-script-based-on-an-event.md), qui illustre l’utilisation de la classe de consommateur standard [**ActiveScriptEventConsumer**](activescripteventconsumer.md) pour configurer un consommateur permanent.</span><span class="sxs-lookup"><span data-stu-id="f3fba-109">For an example of using a logical consumer, see [Running a Script Based on an Event](running-a-script-based-on-an-event.md), which shows the use of the standard consumer class [**ActiveScriptEventConsumer**](activescripteventconsumer.md) to configure a permanent consumer.</span></span>

<span data-ttu-id="f3fba-110">La procédure suivante décrit comment créer un consommateur logique.</span><span class="sxs-lookup"><span data-stu-id="f3fba-110">The following procedure describes how to create a logical consumer.</span></span>

<span data-ttu-id="f3fba-111">**Pour créer un consommateur logique**</span><span class="sxs-lookup"><span data-stu-id="f3fba-111">**To create a logical consumer**</span></span>

1.  <span data-ttu-id="f3fba-112">Créez une instance de votre classe de consommateur permanente.</span><span class="sxs-lookup"><span data-stu-id="f3fba-112">Create an instance of your permanent consumer class.</span></span>
2.  <span data-ttu-id="f3fba-113">Remplissez les propriétés de l’instance avec les paramètres de l’action que le consommateur physique doit effectuer.</span><span class="sxs-lookup"><span data-stu-id="f3fba-113">Fill the properties of the instance with the parameters of the action you want the physical consumer to perform.</span></span>

<span data-ttu-id="f3fba-114">L’exemple de code MOF suivant décrit un consommateur logique qui contient un script.</span><span class="sxs-lookup"><span data-stu-id="f3fba-114">The following MOF code example describes a logical consumer that contains a script.</span></span>

``` syntax
#pragma namespace("\\\\.\\root\\subscription")

instance of ActiveScriptEventConsumer as $CONSUMER
{
    Name = "MyConsumerName";
    ScriptingEngine = "VBScript";
    ScriptText = 

        "Set objFS = CreateObject(\"Scripting.FileSystemObject\")\n"
        "Set objFile = objFS.OpenTextFile(\"C:\\\\ASEC.log\", 8, true);\n"
        "objFile.WriteLine \"Time: \" + new Date() + \";\n"
        "objFile.WriteLine \"Entry made by: \\\"ActiveScript\\\"\";\n"
        "objFile.Close\n";
    
    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

<span data-ttu-id="f3fba-115">Après avoir créé le consommateur logique, vous devez lier chaque filtre à un filtre d’événements pour affecter l’action à un événement particulier.</span><span class="sxs-lookup"><span data-stu-id="f3fba-115">After you create the logical consumer, you must then link each filter to an event filter to assign the action to a particular event.</span></span> <span data-ttu-id="f3fba-116">Pour plus d’informations, consultez [création d’un filtre d’événements](creating-an-event-filter.md).</span><span class="sxs-lookup"><span data-stu-id="f3fba-116">For more information, see [Creating an Event Filter](creating-an-event-filter.md).</span></span>

 

 



