---
description: À l’aide de la classe SMTPEventConsumer, vous pouvez envoyer un e-mail à un utilisateur désigné lorsqu’un événement spécifié se produit. Cette classe est un consommateur d’événements standard fourni par WMI.
ms.assetid: ed10e6f7-8e18-4cde-bd46-a7791547c7da
ms.tgt_platform: multiple
title: Envoi de courrier électronique à partir d’un événement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4929b7c8c29d514d73a6e4c9d14049a19f306233
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106517894"
---
# <a name="sending-email-based-on-an-event"></a><span data-ttu-id="96f70-104">Envoi de courrier électronique à partir d’un événement</span><span class="sxs-lookup"><span data-stu-id="96f70-104">Sending Email Based on an Event</span></span>

<span data-ttu-id="96f70-105">À l’aide de la classe [SMTPEventConsumer](smtpeventconsumer.md) , vous pouvez envoyer un e-mail à un utilisateur désigné lorsqu’un événement spécifié se produit.</span><span class="sxs-lookup"><span data-stu-id="96f70-105">By using the [SMTPEventConsumer](smtpeventconsumer.md) class, you can send email to a designated user when a specified event occurs.</span></span> <span data-ttu-id="96f70-106">Cette classe est un [consommateur d’événements standard](standard-consumer-classes.md) fourni par WMI.</span><span class="sxs-lookup"><span data-stu-id="96f70-106">This class is a [standard event consumer](standard-consumer-classes.md) that WMI provides.</span></span>

<span data-ttu-id="96f70-107">La classe [SMTPEventConsumer](smtpeventconsumer.md) nécessite les conditions suivantes pour envoyer un message électronique en réponse à un événement :</span><span class="sxs-lookup"><span data-stu-id="96f70-107">The [SMTPEventConsumer](smtpeventconsumer.md) class requires the following conditions to send an email message in response to an event:</span></span>

-   <span data-ttu-id="96f70-108">La classe [SMTPEventConsumer](smtpeventconsumer.md) doit être compilée dans l’espace de noms approprié.</span><span class="sxs-lookup"><span data-stu-id="96f70-108">The [SMTPEventConsumer](smtpeventconsumer.md) class must be compiled into the correct namespace.</span></span> <span data-ttu-id="96f70-109">Pour plus d’informations, consultez [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="96f70-109">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>
-   <span data-ttu-id="96f70-110">Un serveur SMTP doit exister sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="96f70-110">An SMTP server must exist on the network.</span></span>
-   <span data-ttu-id="96f70-111">Le message électronique ne peut pas avoir une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="96f70-111">The email message cannot have an attachment.</span></span>
-   <span data-ttu-id="96f70-112">Le message électronique doit être encodé en US-ASCII.</span><span class="sxs-lookup"><span data-stu-id="96f70-112">The email message must be encoded in US-ASCII.</span></span>

<span data-ttu-id="96f70-113">La procédure de base pour l’utilisation de consommateurs standard est toujours la même, et se trouve dans la [surveillance et la réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="96f70-113">The basic procedure for using standard consumers is always the same, and is located in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="96f70-114">La procédure suivante ajoute à la procédure de base. est spécifique à la classe [SMTPEventConsumer](smtpeventconsumer.md) ; et décrit comment créer un consommateur d’événements qui envoie des messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="96f70-114">The following procedure adds to the basic procedure; is specific to the [SMTPEventConsumer](smtpeventconsumer.md) class; and describes how to create an event consumer that sends email.</span></span>

<span data-ttu-id="96f70-115">La procédure suivante décrit comment créer un consommateur d’événements qui envoie des messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="96f70-115">The following procedure describes how to create an event consumer that sends email.</span></span>

<span data-ttu-id="96f70-116">**Pour créer un consommateur d’événements qui envoie des messages électroniques**</span><span class="sxs-lookup"><span data-stu-id="96f70-116">**To create an event consumer that sends email**</span></span>

1.  <span data-ttu-id="96f70-117">Installez et inscrivez la classe [SMTPEventConsumer](smtpeventconsumer.md) , si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="96f70-117">Install and register the [SMTPEventConsumer](smtpeventconsumer.md) class, if necessary.</span></span>

    <span data-ttu-id="96f70-118">La classe [SMTPEventConsumer](smtpeventconsumer.md) est compilée dans l' \\ espace de noms de l’abonnement racine par le programme d’installation de WMI.</span><span class="sxs-lookup"><span data-stu-id="96f70-118">The [SMTPEventConsumer](smtpeventconsumer.md) class is compiled into the root\\subscription namespace by the WMI setup program.</span></span>

2.  <span data-ttu-id="96f70-119">Identifiez l’événement que vous souhaitez surveiller et créez la requête d’événement.</span><span class="sxs-lookup"><span data-stu-id="96f70-119">Identify the event that you want to monitor and create the event query.</span></span>

    <span data-ttu-id="96f70-120">Il peut y avoir un événement intrinsèque existant qui utilise pour surveiller votre événement.</span><span class="sxs-lookup"><span data-stu-id="96f70-120">There might be an existing intrinsic event that use to monitor your event.</span></span> <span data-ttu-id="96f70-121">La plupart des événements intrinsèques sont associés aux modifications apportées aux instances de classe dans l’espace de noms « root \\ cimv2 ».</span><span class="sxs-lookup"><span data-stu-id="96f70-121">Most intrinsic events are associated with changes to class instances in the "root\\cimv2" namespace.</span></span> <span data-ttu-id="96f70-122">En analysant les classes de la référence des [classes WMI](wmi-classes.md) , vous pouvez trouver une classe qui identifie l’événement que vous souhaitez analyser.</span><span class="sxs-lookup"><span data-stu-id="96f70-122">By analyzing the classes in the [WMI Classes](wmi-classes.md) reference, you can probably find a class that identifies the event you want to monitor.</span></span> <span data-ttu-id="96f70-123">Par exemple, utilisez la classe disque [**\_ logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) pour surveiller les modifications apportées à un lecteur de disque dur.</span><span class="sxs-lookup"><span data-stu-id="96f70-123">For example, use the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class to monitor changes to a hard disk drive.</span></span>

    <span data-ttu-id="96f70-124">S’il n’existe aucun événement intrinsèque existant qui utilise, un fournisseur d’événements extrinsèque peut fonctionner.</span><span class="sxs-lookup"><span data-stu-id="96f70-124">If there are no existing intrinsic events that use, there might be an extrinsic event provider that can work.</span></span> <span data-ttu-id="96f70-125">Par exemple, utilisez la classe [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) du fournisseur Registry pour surveiller les modifications apportées au registre système.</span><span class="sxs-lookup"><span data-stu-id="96f70-125">For example, use the [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) class of the Registry provider to monitor changes to the system registry.</span></span>

    <span data-ttu-id="96f70-126">S’il n’existe pas de classe qui identifie l’événement que vous souhaitez analyser, vous devez créer votre propre fournisseur d’événements et définir de nouvelles classes d’événements extrinsèques.</span><span class="sxs-lookup"><span data-stu-id="96f70-126">If a class does not exist that identifies the event you want to monitor, you must create your own event provider and define new extrinsic event classes.</span></span> <span data-ttu-id="96f70-127">Pour plus d’informations, consultez [écriture d’un fournisseur d’événements](writing-an-event-provider.md).</span><span class="sxs-lookup"><span data-stu-id="96f70-127">For more information, see [Writing an Event Provider](writing-an-event-provider.md).</span></span>

3.  <span data-ttu-id="96f70-128">Dans le fichier format MOF (MOF), créez une instance de [SMTPEventConsumer](smtpeventconsumer.md) pour recevoir des événements.</span><span class="sxs-lookup"><span data-stu-id="96f70-128">In the Managed Object Format (MOF) file, create an instance of the [SMTPEventConsumer](smtpeventconsumer.md) to receive events.</span></span>

    <span data-ttu-id="96f70-129">Utilisez les propriétés de l’instance pour définir le message électronique à envoyer lorsqu’un événement se produit.</span><span class="sxs-lookup"><span data-stu-id="96f70-129">Use the properties of the instance to define the email message to send when an event occurs.</span></span> <span data-ttu-id="96f70-130">Par exemple, la propriété **ToLine** définit l’adresse de messagerie et la propriété **message** définit le texte du message électronique.</span><span class="sxs-lookup"><span data-stu-id="96f70-130">For example, the **ToLine** property defines the email address, and the **Message** property defines the text of the email message.</span></span> <span data-ttu-id="96f70-131">Vous devez définir l’adresse de messagerie, l’objet et le texte d’un message, mais un message électronique ne peut pas avoir de pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="96f70-131">You must define the email address, subject, and text of a message, but an email message cannot have an attachment.</span></span> <span data-ttu-id="96f70-132">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="96f70-132">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

4.  <span data-ttu-id="96f70-133">Créez une requête d’événement qui spécifie les événements que vous souhaitez analyser.</span><span class="sxs-lookup"><span data-stu-id="96f70-133">Create an event query that specifies the events you want to monitor.</span></span>

    <span data-ttu-id="96f70-134">Pour plus d’informations, consultez [interrogation avec WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="96f70-134">For more information, see [Querying with WQL](querying-with-wql.md).</span></span>

5.  <span data-ttu-id="96f70-135">Créez une instance de [**\_ \_ EventFilter**](--eventfilter.md) et stockez votre requête dans la propriété de la **requête** .</span><span class="sxs-lookup"><span data-stu-id="96f70-135">Create an instance of [**\_\_EventFilter**](--eventfilter.md) and store your query in the **Query** property.</span></span>

    <span data-ttu-id="96f70-136">Pour plus d’informations, consultez [interrogation avec WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="96f70-136">For more information see, [Querying with WQL](querying-with-wql.md).</span></span>

6.  <span data-ttu-id="96f70-137">Créez une instance de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) pour associer le filtre et le consommateur.</span><span class="sxs-lookup"><span data-stu-id="96f70-137">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter and the consumer.</span></span>
7.  <span data-ttu-id="96f70-138">Compilez le fichier MOF à l’aide de [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="96f70-138">Compile the MOF file by using [**Mofcomp.exe**](mofcomp.md).</span></span>


## <a name="example"></a><span data-ttu-id="96f70-139">Exemple</span><span class="sxs-lookup"><span data-stu-id="96f70-139">Example</span></span>

<span data-ttu-id="96f70-140">L’exemple de cette section se trouve dans le code MOF, mais vous pouvez créer des instances par programme à l’aide [de l’API de script pour WMI](scripting-api-for-wmi.md) ou [de l’API com pour WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="96f70-140">The example in this section is in MOF code, but you can create the instances programmatically by using the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span>

<span data-ttu-id="96f70-141">La procédure suivante décrit comment utiliser l’exemple.</span><span class="sxs-lookup"><span data-stu-id="96f70-141">The following procedure describes how to use the example.</span></span>

<span data-ttu-id="96f70-142">**Pour utiliser l’exemple**</span><span class="sxs-lookup"><span data-stu-id="96f70-142">**To use the example**</span></span>

1.  <span data-ttu-id="96f70-143">Copiez le fichier MOF suivant dans un fichier texte et enregistrez-le avec une extension. mof.</span><span class="sxs-lookup"><span data-stu-id="96f70-143">Copy the following MOF to a text file and save it with a .mof extension.</span></span>
2.  <span data-ttu-id="96f70-144">Dans une fenêtre d’invite de commandes, compilez le fichier MOF à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="96f70-144">In a command prompt window, compile the MOF file by using the following command:</span></span>

    <span data-ttu-id="96f70-145">Fichier **mofcomp** \*\* \* *. mof*\*</span><span class="sxs-lookup"><span data-stu-id="96f70-145">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

> [!Note]  
> <span data-ttu-id="96f70-146">Quand le code MOF est compilé dans l' \\ espace de noms de l’abonnement racine, [SMTPEventConsumer](smtpeventconsumer.md) est compilé dans le même espace de noms.</span><span class="sxs-lookup"><span data-stu-id="96f70-146">When MOF code is compiled into the root\\subscription namespace, the [SMTPEventConsumer](smtpeventconsumer.md) is compiled into the same namespace.</span></span>

 

``` syntax
#pragma namespace ("\\\\.\\root\\subscription")

instance of __EventFilter as $FILTER
{
    Name = "LowDiskspaceFilter";
    
    EventNamespace = "\\\\.\\root\\cimv2";  

    Query = "SELECT * FROM __InstanceModificationEvent WITHIN 10 "
            "WHERE TargetInstance ISA \"Win32_LogicalDisk\" "
            "AND TargetInstance.FreeSpace < 846000000 "
            "AND PreviousInstance.FreeSpace >= 846000000 "
            "AND (TargetInstance.DeviceID = \"C:\" "
            "OR TargetInstance.DeviceID = \"D:\")";
    QueryLanguage = "WQL";
};


instance of SMTPEventConsumer as $CONSUMER
{
    Name = "LowDisk";
    ToLine = "SysAd@MyCompany.com, MyAlias@MyCompany.com";
    CcLine = "MyHome@MyISP.com";
    ReplyToLine = "MyAlias@MyCompany.com";
    SMTPServer = "SmartHost";
    Subject = "WARNING: Low disk space";
    Message = "WARNING: Your %TargetInstance.DeviceID% is"
        " getting dangerously low.";
};

instance of __FilterToConsumerBinding
{
    Consumer = $CONSUMER ;
    Filter = $FILTER ;
};
```

## <a name="related-topics"></a><span data-ttu-id="96f70-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="96f70-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96f70-148">Surveillance et réponse aux événements avec des consommateurs standard</span><span class="sxs-lookup"><span data-stu-id="96f70-148">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
