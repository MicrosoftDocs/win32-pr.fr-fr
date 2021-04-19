---
description: La classe CommandLineEventConsumer exécute un programme exécutable spécifié à partir d’une ligne de commande lorsqu’un événement spécifié se produit. Cette classe est un consommateur d’événements standard fourni par WMI.
ms.assetid: b912a4a1-7b1c-43a9-b098-fcfd62a2c2db
ms.tgt_platform: multiple
title: Exécution d’un programme à partir de la ligne de commande en fonction d’un événement
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: de7f4fb5e679a6b5767635c70e2ffb5eda3ba800
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517612"
---
# <a name="running-a-program-from-the-command-line-based-on-an-event"></a><span data-ttu-id="659c0-104">Exécution d’un programme à partir de la ligne de commande en fonction d’un événement</span><span class="sxs-lookup"><span data-stu-id="659c0-104">Running a Program from the Command Line Based on an Event</span></span>

<span data-ttu-id="659c0-105">La classe [**CommandLineEventConsumer**](commandlineeventconsumer.md) exécute un programme exécutable spécifié à partir d’une ligne de commande lorsqu’un événement spécifié se produit.</span><span class="sxs-lookup"><span data-stu-id="659c0-105">The [**CommandLineEventConsumer**](commandlineeventconsumer.md) class runs a specified executable program from a command line when a specified event occurs.</span></span> <span data-ttu-id="659c0-106">Cette classe est un consommateur d’événements standard fourni par WMI.</span><span class="sxs-lookup"><span data-stu-id="659c0-106">This class is a standard event consumer that WMI provides.</span></span>

<span data-ttu-id="659c0-107">Lorsque vous utilisez [**CommandLineEventConsumer**](commandlineeventconsumer.md), vous devez sécuriser l’exécutable que vous souhaitez démarrer.</span><span class="sxs-lookup"><span data-stu-id="659c0-107">When you use [**CommandLineEventConsumer**](commandlineeventconsumer.md), you should secure the executable that you want to start.</span></span> <span data-ttu-id="659c0-108">Si l’exécutable ne se trouve pas dans un emplacement sécurisé ou n’est pas sécurisé avec une liste de contrôle d’accès (ACL) forte, un utilisateur sans privilèges d’accès peut remplacer votre exécutable par un autre exécutable.</span><span class="sxs-lookup"><span data-stu-id="659c0-108">If the executable is not in a secure location or not secured with a strong access control list (ACL), a user without access privileges can replace your executable with a different executable.</span></span> <span data-ttu-id="659c0-109">Vous pouvez utiliser les classes [**Win32 \_ LogicalFileSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting) ou [**Win32 \_ LogicalShareSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting) pour modifier par programmation la sécurité d’un fichier ou d’un partage.</span><span class="sxs-lookup"><span data-stu-id="659c0-109">You can use the [**Win32\_LogicalFileSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting) or [**Win32\_LogicalShareSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting) classes to change programmatically the security of a file or share.</span></span> <span data-ttu-id="659c0-110">Pour plus d’informations, consultez [création d’un descripteur de sécurité pour un nouvel objet en C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="659c0-110">For more information, see [Creating a Security Descriptor for a New Object in C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

<span data-ttu-id="659c0-111">La procédure de base pour utiliser des consommateurs standard est toujours la même et se trouve dans [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="659c0-111">The basic procedure to use standard consumers is always the same, and is located in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="659c0-112">La procédure suivante ajoute à la procédure de base, est spécifique à la classe [**CommandLineEventConsumer**](commandlineeventconsumer.md) et décrit comment créer un consommateur d’événements qui exécute un programme.</span><span class="sxs-lookup"><span data-stu-id="659c0-112">The following procedure adds to the basic procedure, is specific to the [**CommandLineEventConsumer**](commandlineeventconsumer.md) class, and describes how to create an event consumer that runs a program.</span></span>

> [!Caution]
>
> <span data-ttu-id="659c0-113">La classe [**CommandLineEventConsumer**](commandlineeventconsumer.md) a des contraintes de sécurité spéciales.</span><span class="sxs-lookup"><span data-stu-id="659c0-113">The [**CommandLineEventConsumer**](commandlineeventconsumer.md) class has special security constraints.</span></span> <span data-ttu-id="659c0-114">Ce consommateur standard doit être configuré par un membre local du groupe Administrateurs sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="659c0-114">This standard consumer must be configured by a local member of the Administrators group on the local computer.</span></span> <span data-ttu-id="659c0-115">Si vous utilisez un compte de domaine pour créer l’abonnement, le compte LocalSystem doit disposer des autorisations nécessaires sur le domaine pour vérifier que le créateur est membre du groupe Administrateurs local.</span><span class="sxs-lookup"><span data-stu-id="659c0-115">If you use a domain account to create the subscription, the LocalSystem account must have the necessary permissions on the domain to verify that the creator is a member of the local Administrators group.</span></span>
>
> <span data-ttu-id="659c0-116">[**CommandLineEventConsumer**](commandlineeventconsumer.md) ne peut pas être utilisé pour démarrer un processus qui s’exécute de manière interactive.</span><span class="sxs-lookup"><span data-stu-id="659c0-116">[**CommandLineEventConsumer**](commandlineeventconsumer.md) cannot be used to start a process that runs interactively.</span></span>

 

<span data-ttu-id="659c0-117">La procédure suivante décrit comment créer un consommateur d’événements qui exécute un processus à partir d’une ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="659c0-117">The following procedure describes how to create an event consumer that runs a process from a command line.</span></span>

<span data-ttu-id="659c0-118">**Pour créer un consommateur d’événements qui exécute un processus à partir d’une ligne de commande**</span><span class="sxs-lookup"><span data-stu-id="659c0-118">**To create an event consumer that runs a process from a command line**</span></span>

1.  <span data-ttu-id="659c0-119">Dans le fichier format MOF (MOF), créez une instance de [**CommandLineEventConsumer**](commandlineeventconsumer.md) pour recevoir les événements que vous demandez dans la requête.</span><span class="sxs-lookup"><span data-stu-id="659c0-119">In the Managed Object Format (MOF) file, create an instance of [**CommandLineEventConsumer**](commandlineeventconsumer.md) to receive the events you request in the query.</span></span> <span data-ttu-id="659c0-120">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="659c0-120">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>
2.  <span data-ttu-id="659c0-121">Créez une instance de [**\_ \_ EventFilter**](--eventfilter.md) et donnez-lui un nom.</span><span class="sxs-lookup"><span data-stu-id="659c0-121">Create an instance of [**\_\_EventFilter**](--eventfilter.md) and give it a name.</span></span>
3.  <span data-ttu-id="659c0-122">Créez une requête pour spécifier le type d’événement.</span><span class="sxs-lookup"><span data-stu-id="659c0-122">Create a query to specify the type of event.</span></span> <span data-ttu-id="659c0-123">Pour plus d’informations, consultez [interrogation avec WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="659c0-123">For more information, see [Querying with WQL](querying-with-wql.md).</span></span>
4.  <span data-ttu-id="659c0-124">Créez une instance de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) pour associer le filtre à l’instance de [**CommandLineEventConsumer**](commandlineeventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="659c0-124">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter with the instance of [**CommandLineEventConsumer**](commandlineeventconsumer.md).</span></span>
5.  <span data-ttu-id="659c0-125">Compilez votre fichier MOF à l’aide de [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="659c0-125">Compile your MOF file by using [**Mofcomp.exe**](mofcomp.md).</span></span>

## <a name="example"></a><span data-ttu-id="659c0-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="659c0-126">Example</span></span>

<span data-ttu-id="659c0-127">L’exemple de code suivant crée une nouvelle classe appelée « MyCmdLineConsumer » pour générer des événements lorsqu’une instance de la nouvelle classe est créée à la fin d’un MOF.</span><span class="sxs-lookup"><span data-stu-id="659c0-127">The following code example creates a new class called "MyCmdLineConsumer" to generate events when an instance of the new class is created at the end of a MOF.</span></span> <span data-ttu-id="659c0-128">L’exemple se trouve dans du code MOF, mais vous pouvez créer des instances par programme à l’aide [de l’API de script pour WMI](scripting-api-for-wmi.md) ou de l' [API com pour WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="659c0-128">The example is in MOF code, but you can create the instances programmatically by using the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span>

<span data-ttu-id="659c0-129">La procédure suivante décrit comment créer une nouvelle classe appelée MyCmdLineConsumer.</span><span class="sxs-lookup"><span data-stu-id="659c0-129">The following procedure describes how to create a new class called MyCmdLineConsumer.</span></span>

<span data-ttu-id="659c0-130">**Pour créer une nouvelle classe appelée MyCmdLineConsumer**</span><span class="sxs-lookup"><span data-stu-id="659c0-130">**To create a new class called MyCmdLineConsumer**</span></span>

1.  <span data-ttu-id="659c0-131">Créez le fichier de \\test.bat c : cmdline \_ avec une commande qui exécute un programme visible, tel que « calc.exe ».</span><span class="sxs-lookup"><span data-stu-id="659c0-131">Create the c:\\cmdline\_test.bat file with a command that executes a visible program, such as "calc.exe" .</span></span>
2.  <span data-ttu-id="659c0-132">Copiez le fichier MOF dans un fichier texte et enregistrez-le avec une extension. mof.</span><span class="sxs-lookup"><span data-stu-id="659c0-132">Copy the MOF to a text file and save it with a .mof extension.</span></span>
3.  <span data-ttu-id="659c0-133">Dans un Fenêtre Commande, compilez le fichier MOF à l’aide de la commande suivante : **mofcomp nom_fichier. mof**.</span><span class="sxs-lookup"><span data-stu-id="659c0-133">In a Command window, compile the MOF file by using the following command: **Mofcomp filename.mof**.</span></span>

> [!Note]  
> <span data-ttu-id="659c0-134">Le programme spécifié dans cmdline \_test.bat doit s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="659c0-134">The program specified in cmdline\_test.bat should execute.</span></span>

 

``` syntax
// Set the namespace as root\subscription.
// The CommandLineEventConsumer is already compiled
// in the root\subscription namespace. 
#pragma namespace ("\\\\.\\Root\\subscription")

class MyCmdLineConsumer
{
 [key]string Name;
};

// Create an instance of the command line consumer
// and give it the alias $CMDLINECONSUMER

instance of CommandLineEventConsumer as $CMDLINECONSUMER
{
 Name = "CmdLineConsumer_Example";
 CommandLineTemplate = "c:\\cmdline_test.bat";
 RunInteractively = True;
 WorkingDirectory = "c:\\";
};    

// Create an instance of the event filter
// and give it the alias $CMDLINEFILTER
// The filter queries for instance creation event
// for instances of the MyCmdLineConsumer class

instance of __EventFilter as $CMDLINEFILTER
{
    Name = "CmdLineFilter";
    Query = "SELECT * FROM __InstanceCreationEvent"
        " WHERE TargetInstance.__class = \"MyCmdLineConsumer\"";
    QueryLanguage = "WQL";
};

// Create an instance of the binding
// between filter and consumer instances.

instance of __FilterToConsumerBinding
{
     Consumer = $CMDLINECONSUMER;
     Filter = $CMDLINEFILTER;
};

// Create an instance of this class right now. 
// The commands in c:\\cmdline_test.bat execute
// as the result of creating the instance
// of MyCmdLineConsumer.
 
instance of MyCmdLineConsumer
{
     Name = "CmdLineEventConsumer test";
};
```

## <a name="related-topics"></a><span data-ttu-id="659c0-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="659c0-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="659c0-136">Surveillance et réponse aux événements avec des consommateurs standard</span><span class="sxs-lookup"><span data-stu-id="659c0-136">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
