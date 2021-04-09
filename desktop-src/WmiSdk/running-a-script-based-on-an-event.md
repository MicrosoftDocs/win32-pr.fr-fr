---
description: Le consommateur standard implémenté par la classe ActiveScriptEventConsumer permet à un ordinateur d’exécuter un script et de prendre des mesures lorsque des événements importants se produisent pour s’assurer qu’un ordinateur peut détecter et résoudre les problèmes automatiquement.
ms.assetid: 0d2ac139-3e2b-4089-ae9c-289d376e27a2
ms.tgt_platform: multiple
title: Exécution d’un script basé sur un événement
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4dbb1e55c7828a79d6541182eff5ce20147a82c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868133"
---
# <a name="running-a-script-based-on-an-event"></a><span data-ttu-id="c31c6-103">Exécution d’un script basé sur un événement</span><span class="sxs-lookup"><span data-stu-id="c31c6-103">Running a Script Based on an Event</span></span>

<span data-ttu-id="c31c6-104">Le consommateur standard implémenté par la classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) permet à un ordinateur d’exécuter un script et de prendre des mesures lorsque des événements importants se produisent pour s’assurer qu’un ordinateur peut détecter et résoudre les problèmes automatiquement.</span><span class="sxs-lookup"><span data-stu-id="c31c6-104">The standard consumer that is implemented by the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class allows a computer to run a script and take action when important events occur to ensure that a computer can detect and resolve problems automatically.</span></span>

<span data-ttu-id="c31c6-105">Ce consommateur est chargé par défaut dans l’espace de noms de l' **\\ abonnement racine** .</span><span class="sxs-lookup"><span data-stu-id="c31c6-105">This consumer is loaded by default in the **root\\subscription** namespace.</span></span>

<span data-ttu-id="c31c6-106">Vous pouvez configurer les performances de toutes les instances de [**ActiveScriptEventConsumer**](activescripteventconsumer.md) sur un système en définissant les valeurs de la propriété **timeout** ou **MaximumScripts** dans une seule instance de [**ScriptingStandardConsumerSetting**](scriptingstandardconsumersetting.md).</span><span class="sxs-lookup"><span data-stu-id="c31c6-106">You can configure the performance of all instances of [**ActiveScriptEventConsumer**](activescripteventconsumer.md) on a system by setting the values of the **Timeout** or **MaximumScripts** property in a single instance of [**ScriptingStandardConsumerSetting**](scriptingstandardconsumersetting.md).</span></span>

<span data-ttu-id="c31c6-107">La procédure de base pour l’utilisation de consommateurs standard est toujours la même, et se trouve dans la [surveillance et la réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="c31c6-107">The basic procedure for using standard consumers is always the same, and is located in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="c31c6-108">La procédure suivante, qui ajoute à la procédure de base, est spécifique à la classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) et décrit comment créer un consommateur d’événements qui exécute un script.</span><span class="sxs-lookup"><span data-stu-id="c31c6-108">The following procedure that adds to the basic procedure, is specific to the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class, and describes how to create an event consumer that runs a script.</span></span>

> [!Caution]  
> <span data-ttu-id="c31c6-109">La classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) a des contraintes de sécurité spéciales.</span><span class="sxs-lookup"><span data-stu-id="c31c6-109">The [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class has special security constraints.</span></span> <span data-ttu-id="c31c6-110">Ce consommateur standard doit être configuré par un membre local du groupe Administrateurs sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="c31c6-110">This standard consumer must be configured by a local member of the Administrators group on the local computer.</span></span> <span data-ttu-id="c31c6-111">Si vous utilisez un compte de domaine pour créer l’abonnement, le compte LocalSystem doit disposer des autorisations nécessaires sur le domaine pour vérifier que le créateur est membre du groupe Administrateurs local.</span><span class="sxs-lookup"><span data-stu-id="c31c6-111">If you use a domain account to create the subscription, the LocalSystem account must have the necessary permissions on the domain to verify that the creator is a member of the local Administrators group.</span></span>

 

<span data-ttu-id="c31c6-112">La procédure suivante décrit comment créer un consommateur d’événements qui exécute un script.</span><span class="sxs-lookup"><span data-stu-id="c31c6-112">The following procedure describes how to create an event consumer that executes a script.</span></span>

<span data-ttu-id="c31c6-113">**Pour créer un consommateur d’événements qui exécute un script**</span><span class="sxs-lookup"><span data-stu-id="c31c6-113">**To create an event consumer that executes a script**</span></span>

1.  <span data-ttu-id="c31c6-114">Écrivez le script à exécuter lorsqu’un événement se produit.</span><span class="sxs-lookup"><span data-stu-id="c31c6-114">Write the script to run when an event takes place.</span></span>

    <span data-ttu-id="c31c6-115">Vous pouvez écrire le script dans n’importe quel langage, mais assurez-vous qu’un moteur de script pour le langage que vous choisissez est installé sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c31c6-115">You can write the script in any language, but ensure that a scripting engine for the language that you choose is installed on your machine.</span></span> <span data-ttu-id="c31c6-116">Le script n’a pas besoin d’utiliser les objets de script WMI.</span><span class="sxs-lookup"><span data-stu-id="c31c6-116">The script does not have to use WMI scripting objects.</span></span>

    <span data-ttu-id="c31c6-117">Seul un administrateur peut configurer un consommateur de script et le script s’exécute sous les informations d’identification LocalSystem, ce qui offre aux consommateurs des fonctionnalités étendues, à l’exception de l’accès réseau.</span><span class="sxs-lookup"><span data-stu-id="c31c6-117">Only an administrator can set up a script consumer, and the script runs under LocalSystem credentials, which gives broad capabilities to the consumer except for network access.</span></span> <span data-ttu-id="c31c6-118">Toutefois, le script n’a pas accès à des données d’ouverture de session utilisateur spécifiques, par exemple, des variables d’environnement et des partages réseau.</span><span class="sxs-lookup"><span data-stu-id="c31c6-118">However, the script does not have access to specific user logon data, for example, environment variables and network shares.</span></span>

2.  <span data-ttu-id="c31c6-119">Dans le fichier format MOF (MOF), créez une instance de [**ActiveScriptEventConsumer**](activescripteventconsumer.md) pour recevoir les événements que vous demandez dans la requête.</span><span class="sxs-lookup"><span data-stu-id="c31c6-119">In the Managed Object Format (MOF) file, create an instance of [**ActiveScriptEventConsumer**](activescripteventconsumer.md) to receive the events you request in the query.</span></span>

    <span data-ttu-id="c31c6-120">Vous pouvez placer le texte du script dans **ScriptText**, ou vous pouvez spécifier le chemin d’accès et le nom de fichier du script dans **ScriptFileName**.</span><span class="sxs-lookup"><span data-stu-id="c31c6-120">You can put the text of the script in **ScriptText**, or you can specify the path and filename of the script in **ScriptFileName**.</span></span> <span data-ttu-id="c31c6-121">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="c31c6-121">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

3.  <span data-ttu-id="c31c6-122">Créez une instance de [**\_ \_ EventFilter**](--eventfilter.md), nommez-la, puis créez une requête pour spécifier le type d’événement, qui déclenche l’exécution du script.</span><span class="sxs-lookup"><span data-stu-id="c31c6-122">Create an instance of [**\_\_EventFilter**](--eventfilter.md), name it, and then create a query to specify the type of event, which triggers executing the script.</span></span>

    <span data-ttu-id="c31c6-123">Pour plus d’informations, consultez [interrogation avec WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="c31c6-123">For more information see, [Querying with WQL](querying-with-wql.md).</span></span>

4.  <span data-ttu-id="c31c6-124">Créez une instance de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) pour associer le filtre à l’instance de [**ActiveScriptEventConsumer**](activescripteventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="c31c6-124">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter with the instance of [**ActiveScriptEventConsumer**](activescripteventconsumer.md).</span></span>
5.  <span data-ttu-id="c31c6-125">Compilez le fichier MOF à l’aide de [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="c31c6-125">Compile the MOF file by using [**Mofcomp.exe**](mofcomp.md).</span></span>

<span data-ttu-id="c31c6-126">Les exemples de la section suivante présentent deux façons d’implémenter un script piloté par les événements.</span><span class="sxs-lookup"><span data-stu-id="c31c6-126">The examples in the following section show two ways to implement an event-driven script.</span></span> <span data-ttu-id="c31c6-127">Le premier exemple utilise un script défini dans un fichier externe, et le deuxième exemple utilise un script intégré au code MOF.</span><span class="sxs-lookup"><span data-stu-id="c31c6-127">The first example uses a script that is defined in an external file, and the second example uses a script that is built into the MOF code.</span></span> <span data-ttu-id="c31c6-128">Les exemples se trouvent dans du code MOF, mais vous pouvez créer des instances par programme à l’aide [de l’API de script pour WMI](scripting-api-for-wmi.md) ou de l' [API com pour WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="c31c6-128">The examples are in MOF code, but you can create the instances programmatically by using either the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span>

## <a name="example-using-an-external-script"></a><span data-ttu-id="c31c6-129">Exemple utilisant un script externe</span><span class="sxs-lookup"><span data-stu-id="c31c6-129">Example Using an External Script</span></span>

<span data-ttu-id="c31c6-130">La procédure suivante décrit comment utiliser l’exemple de script externe.</span><span class="sxs-lookup"><span data-stu-id="c31c6-130">The following procedure describes how to use the external script example.</span></span>

<span data-ttu-id="c31c6-131">**Pour utiliser l’exemple de script externe**</span><span class="sxs-lookup"><span data-stu-id="c31c6-131">**To use the external script example**</span></span>

1.  <span data-ttu-id="c31c6-132">Créez un fichier nommé c : \\Asec.vbs, puis copiez le script dans cet exemple dans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="c31c6-132">Create a file named c:\\Asec.vbs, and then copy the script in this example into it.</span></span>
2.  <span data-ttu-id="c31c6-133">Copiez la liste MOF dans un fichier texte et enregistrez-la avec une extension. mof.</span><span class="sxs-lookup"><span data-stu-id="c31c6-133">Copy the MOF list into a text file and save it with a .mof extension.</span></span>
3.  <span data-ttu-id="c31c6-134">Dans une fenêtre d’invite de commandes, compilez le fichier MOF à l’aide de la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="c31c6-134">In a command prompt window, compile the MOF file by using the following command.</span></span>

    <span data-ttu-id="c31c6-135">Fichier **mofcomp** \*\* \* *. mof*\*</span><span class="sxs-lookup"><span data-stu-id="c31c6-135">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

4.  <span data-ttu-id="c31c6-136">Exécutez la calculatrice, qui crée un processus de calc.exe.</span><span class="sxs-lookup"><span data-stu-id="c31c6-136">Run the Calculator, which creates a calc.exe process.</span></span> <span data-ttu-id="c31c6-137">Attendez plus de cinq secondes, fermez la fenêtre calculatrice, puis recherchez \\ un fichier nommé ASEC. log dans le répertoire C :.</span><span class="sxs-lookup"><span data-stu-id="c31c6-137">Wait for more than five seconds, close the Calculator window, and then look in the C:\\ directory for a file named ASEC.log.</span></span>

    <span data-ttu-id="c31c6-138">Le texte suivant est similaire au texte qui sera contenu dans le fichier ASEC. log.</span><span class="sxs-lookup"><span data-stu-id="c31c6-138">The following text is similar to the text that will be contained in the ASEC.log file.</span></span>

    ``` syntax
    Time: 12/31/2002 2:56:33 PM; Entry made by: ASEC
    Application closed. UserModeTime:  1562500; 
    KernelModeTime: 3125000 [hundreds of nanoseconds]
    ```

<span data-ttu-id="c31c6-139">L’exemple de code VBScript suivant montre le script qui est appelé lorsqu’un événement est reçu par le consommateur permanent.</span><span class="sxs-lookup"><span data-stu-id="c31c6-139">The following VBScript code example shows the script that is called when an event is received by the permanent consumer.</span></span> <span data-ttu-id="c31c6-140">L’objet **TargetEvent** est une instance [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md) , de sorte qu’il possède une propriété nommée **TargetInstance**, qui est une instance de [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) utilisée pour déclencher l’événement.</span><span class="sxs-lookup"><span data-stu-id="c31c6-140">The **TargetEvent** object is an [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md) instance so it has a property named **TargetInstance**, which is a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) instance used to fire the event.</span></span> <span data-ttu-id="c31c6-141">La classe de **\_ processus Win32** a les propriétés **UserModeTime** et **KernelModeTime** qui sont placées dans le fichier journal créé par le script.</span><span class="sxs-lookup"><span data-stu-id="c31c6-141">The **Win32\_Process** class has the **UserModeTime** and **KernelModeTime** properties that are put into the log file created by the script.</span></span>


```VB
' asec.vbs script
Dim objFS, objFile
Set objFS = CreateObject("Scripting.FileSystemObject")
Set objFile = objFS.OpenTextFile("C:\ASEC.log", 8, true)
objFile.WriteLine "Time: " & Now & "; Entry made by: ASEC"

objFile.WriteLine "Application closed. UserModeTime:  " & _
    TargetEvent.TargetInstance.UserModeTime & _
    "; KernelModeTime: " & _
    TargetEvent.TargetInstance.KernelModeTime & _
    " [hundreds of nanoseconds]"
objFile.Close
```



<span data-ttu-id="c31c6-142">L’exemple de code MOF suivant appelle le script lorsqu’un événement est reçu.</span><span class="sxs-lookup"><span data-stu-id="c31c6-142">The following MOF code example calls the script when an event is received.</span></span> <span data-ttu-id="c31c6-143">Il crée le filtre, le consommateur et la liaison entre eux dans l’espace de noms de l' **\\ abonnement racine** .</span><span class="sxs-lookup"><span data-stu-id="c31c6-143">It creates the filter, consumer, and the binding between them in the **root\\subscription** namespace.</span></span>

``` syntax
#pragma namespace ("\\\\.\\root\\subscription")

instance of ActiveScriptEventConsumer as $Cons
{
    Name = "ASEC";
    ScriptingEngine = "VBScript";
    ScriptFileName = "c:\\asec2.vbs";
};

instance of __EventFilter as $Filt
{
    Name = "EF";
    Query = "SELECT * FROM __InstanceDeletionEvent WITHIN 5 "
        "WHERE TargetInstance ISA \"Win32_Process\" "
        "AND TargetInstance.Name = \"calc.exe\"";
    QueryLanguage = "WQL";
    EventNamespace = "root\\cimv2";
};

instance of __FilterToConsumerBinding
{
    Filter = $Filt;
    Consumer = $Cons;
};
```

## <a name="example-using-inline-script"></a><span data-ttu-id="c31c6-144">Exemple utilisant un script inline</span><span class="sxs-lookup"><span data-stu-id="c31c6-144">Example Using Inline Script</span></span>

<span data-ttu-id="c31c6-145">La procédure suivante décrit comment utiliser l’exemple de script inline.</span><span class="sxs-lookup"><span data-stu-id="c31c6-145">The following procedure describes how to use the inline script example.</span></span>

<span data-ttu-id="c31c6-146">**Pour utiliser l’exemple de script inline**</span><span class="sxs-lookup"><span data-stu-id="c31c6-146">**To use the inline script example**</span></span>

1.  <span data-ttu-id="c31c6-147">Copiez la liste MOF de cette section dans un fichier texte, puis enregistrez-la avec une extension. mof.</span><span class="sxs-lookup"><span data-stu-id="c31c6-147">Copy the MOF list in this section into a text file, and save it with a .mof extension.</span></span>
2.  <span data-ttu-id="c31c6-148">Dans une fenêtre d’invite de commandes, compilez le fichier MOF à l’aide de la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="c31c6-148">In a command prompt window, compile the MOF file by using the following command.</span></span>

    <span data-ttu-id="c31c6-149">Fichier **mofcomp** \*\* \* *. mof*\*</span><span class="sxs-lookup"><span data-stu-id="c31c6-149">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

<span data-ttu-id="c31c6-150">L’exemple de code MOF suivant crée le filtre, le consommateur et la liaison entre eux et contient également le script inline.</span><span class="sxs-lookup"><span data-stu-id="c31c6-150">The following MOF code example creates the filter, consumer, and the binding between them and also contains the script inline.</span></span>

``` syntax
#pragma namespace ("\\\\.\\root\\subscription")

instance of ActiveScriptEventConsumer as $Cons
{
    Name = "ASEC";
    ScriptingEngine = "VBScript";
    
    ScriptText =
        "Dim objFS, objFile\n"
        "Set objFS = CreateObject(\"Scripting.FileSystemObject\")\n"
        "Set objFile = objFS.OpenTextFile(\"C:\\ASEC.log\","
        " 8, true)\nobjFile.WriteLine \"Time: \" & Now & \";"
        " Entry made by: ASEC\"\nobjFile.WriteLine"
        " \"Application closed. UserModeTime:  \" & "
        "TargetEvent.TargetInstance.UserModeTime &_\n"
        "\"; KernelModeTime: \" & "
        "TargetEvent.TargetInstance.KernelModeTime "
        "& \" [hundreds of nanoseconds]\"\n"
        "objFile.Close\n";
};

instance of __EventFilter as $Filt
{
    Name = "EF";
    Query = "SELECT * FROM __InstanceDeletionEvent WITHIN 5 "
        "WHERE TargetInstance ISA \"Win32_Process\" "
        "AND TargetInstance.Name = \"calc.exe\"";
    QueryLanguage = "WQL";
    EventNamespace = "root\\cimv2";
};

instance of __FilterToConsumerBinding
{
    Filter = $Filt;
    Consumer = $Cons;
};
```

## <a name="related-topics"></a><span data-ttu-id="c31c6-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c31c6-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c31c6-152">Surveillance et réponse aux événements avec des consommateurs standard</span><span class="sxs-lookup"><span data-stu-id="c31c6-152">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
