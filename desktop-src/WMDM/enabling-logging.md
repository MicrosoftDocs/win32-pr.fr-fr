---
title: Activation de la journalisation
description: Activation de la journalisation
ms.assetid: 50fc1d71-b650-4ba5-a6e1-631c0b9fe8ad
keywords:
- Gestionnaire de périphériques Windows Media, journalisation
- Gestionnaire de périphériques, journalisation
- applications de bureau, journalisation
- fournisseurs de services, journalisation
- Guide de programmation, journalisation
- journalisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e95be13e93a5a58bb728d5600c6fdea9801ec2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512240"
---
# <a name="enabling-logging"></a><span data-ttu-id="2439b-109">Activation de la journalisation</span><span class="sxs-lookup"><span data-stu-id="2439b-109">Enabling Logging</span></span>

<span data-ttu-id="2439b-110">Windows Media Gestionnaire de périphériques fournit un objet de journalisation qui peut enregistrer des informations dans un fichier texte au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="2439b-110">Windows Media Device Manager provides a logging object that can save information to a text file at run time.</span></span> <span data-ttu-id="2439b-111">Les développeurs des applications et des fournisseurs de services peuvent utiliser cet objet pour stocker des messages dans un fichier journal pendant l’exécution de leur application ou du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="2439b-111">Developers of both applications and service providers can use this object to store messages in a log file while their application or service provider is running.</span></span> <span data-ttu-id="2439b-112">Cet objet est particulièrement utile lors de la gestion des fichiers protégés par DRM, car Windows Media Gestionnaire de périphériques ne vous permet pas de joindre un débogueur à un processus qui gère des fichiers protégés par DRM.</span><span class="sxs-lookup"><span data-stu-id="2439b-112">This object is especially useful when handling DRM-protected files, because Windows Media Device Manager will not allow you to attach a debugger to a process that is handling DRM-protected files.</span></span>

<span data-ttu-id="2439b-113">L’enregistreur d’événements est un objet COM avec l’ID de classe CLSID \_ WMDMLogger qui expose une interface, [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger).</span><span class="sxs-lookup"><span data-stu-id="2439b-113">The logger is a COM object with the class ID CLSID\_WMDMLogger that exposes one interface, [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger).</span></span> <span data-ttu-id="2439b-114">Les composants n’ont pas besoin d’un certificat pour utiliser l’objet de journalisation.</span><span class="sxs-lookup"><span data-stu-id="2439b-114">Components do not need a certificate to use the logging object.</span></span>

<span data-ttu-id="2439b-115">Par défaut, Windows Media Gestionnaire de périphériques gère un fichier journal, qu’une application utilise ou non **IWMDMLogger**.</span><span class="sxs-lookup"><span data-stu-id="2439b-115">By default, Windows Media Device Manager maintains a log file, regardless of whether an application uses **IWMDMLogger**.</span></span> <span data-ttu-id="2439b-116">Ce fichier journal est un fichier texte simple, et chaque entrée comprend une entrée précédée d’un horodatage au format aaaammjjhhmmss, utilisant une heure locale de 24 heures.</span><span class="sxs-lookup"><span data-stu-id="2439b-116">This log file is a simple text file, and each entry includes an entry preceded by a time stamp in the format YYYYMMDDHHMMSS, using 24-hour local time.</span></span> <span data-ttu-id="2439b-117">Windows Media Gestionnaire de périphériques journalise tous les appels d’API, ainsi que toutes les entrées que vous ajoutez en appelant des messages **IWMDMLogger** .</span><span class="sxs-lookup"><span data-stu-id="2439b-117">Windows Media Device Manager logs all API calls, along with any entries you add by calling **IWMDMLogger** messages.</span></span> <span data-ttu-id="2439b-118">Toutes les entrées de fichier journal sont ajoutées au fichier jusqu’à ce que la [**réinitialisation**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-reset) soit appelée ou que le fichier dépasse sa taille maximale.</span><span class="sxs-lookup"><span data-stu-id="2439b-118">All log file entries are appended to the file until [**Reset**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-reset) is called, or the file exceeds its maximum size.</span></span> <span data-ttu-id="2439b-119">Le fichier est fermé automatiquement après chaque opération de journalisation.</span><span class="sxs-lookup"><span data-stu-id="2439b-119">The file is closed automatically after each logging operation.</span></span> <span data-ttu-id="2439b-120">Le même fichier journal est utilisé pour les entrées d’application et les entrées système.</span><span class="sxs-lookup"><span data-stu-id="2439b-120">The same log file is used for application entries and system entries.</span></span>

<span data-ttu-id="2439b-121">Les étapes suivantes montrent comment utiliser l’objet de journalisation :</span><span class="sxs-lookup"><span data-stu-id="2439b-121">The following steps show how to use the logging object:</span></span>

1.  <span data-ttu-id="2439b-122">Incluez wmdmlog. h dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="2439b-122">Include wmdmlog.h in your project.</span></span>
2.  <span data-ttu-id="2439b-123">Créez un objet de journalisation en appelant **CoCreateInstance**(CLSID \_ WMDMLogger) et en demandant l’interface **IWMDMLogger** .</span><span class="sxs-lookup"><span data-stu-id="2439b-123">Create a logging object by calling **CoCreateInstance**(CLSID\_WMDMLogger) and requesting the **IWMDMLogger** interface.</span></span> <span data-ttu-id="2439b-124">Assignez le pointeur d’interface à une variable globale.</span><span class="sxs-lookup"><span data-stu-id="2439b-124">Assign the interface pointer to a global variable.</span></span>
3.  <span data-ttu-id="2439b-125">Vérifiez que la journalisation est activée en appelant [**IWMDMLogger :: IsEnabled**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-isenabled); Si ce n’est pas le cas, activez-le en appelant [**IWMDMLogger :: Enable**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-enable).</span><span class="sxs-lookup"><span data-stu-id="2439b-125">Verify that logging is enabled by calling [**IWMDMLogger::IsEnabled**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-isenabled); if it is not, enable it by calling [**IWMDMLogger::Enable**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-enable).</span></span>
4.  <span data-ttu-id="2439b-126">Spécifiez un nom et une taille de fichier journal personnalisés.</span><span class="sxs-lookup"><span data-stu-id="2439b-126">Specify a custom log file name and size.</span></span> <span data-ttu-id="2439b-127">Pour ce faire, appelez [**IWMDMLogger :: SetLogFileName**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setlogfilename) et [**IWMDMLogger :: SetSizeParams**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setsizeparams).</span><span class="sxs-lookup"><span data-stu-id="2439b-127">This is done by calling [**IWMDMLogger::SetLogFileName**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setlogfilename) and [**IWMDMLogger::SetSizeParams**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setsizeparams).</span></span>
5.  <span data-ttu-id="2439b-128">À des points de votre code où vous souhaitez créer une entrée dans le journal, appelez [**IWMDMLogger :: LogDword**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logdword) pour consigner des chaînes contenant des variables (cette méthode est similaire à **wsprintf** dans le sens où elle vous permet de mettre en forme une chaîne contenant une valeur de variable), ou appelez [**IWMDMLogger :: LogString**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logstring) pour enregistrer des chaînes constantes.</span><span class="sxs-lookup"><span data-stu-id="2439b-128">At points in your code where you want to make an entry in the log, call either [**IWMDMLogger::LogDword**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logdword) to log strings containing variables (this method is similar to **wsprintf** in the way it allows you to format a string containing a variable value), or call [**IWMDMLogger::LogString**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logstring) to log constant strings.</span></span>

<span data-ttu-id="2439b-129">Pour obtenir un exemple de code, consultez les pages de référence pour les méthodes de [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger).</span><span class="sxs-lookup"><span data-stu-id="2439b-129">For example code, see the reference pages for the methods of [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2439b-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2439b-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2439b-131">**Tâches communes aux applications et aux fournisseurs de services**</span><span class="sxs-lookup"><span data-stu-id="2439b-131">**Tasks Common to Applications and Service Providers**</span></span>](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




