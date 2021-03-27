---
description: Cette rubrique explique comment utiliser le vérificateur de type de fichier fourni dans le kit de développement logiciel (SDK) Windows 7.
ms.assetid: 96FCA74B-DEB2-49D1-B670-EBD8BE0783F1
title: Utilisation du vérificateur de type de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f083897499f972f945867a0c02318df192e734d9
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/28/2021
ms.locfileid: "104211139"
---
# <a name="how-to-use-the-file-type-verifier"></a><span data-ttu-id="33d13-103">Utilisation du vérificateur de type de fichier</span><span class="sxs-lookup"><span data-stu-id="33d13-103">How to Use the File Type Verifier</span></span>

<span data-ttu-id="33d13-104">Cette rubrique explique comment utiliser le vérificateur de type de fichier fourni dans le kit de [développement logiciel (SDK) Windows 7](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="33d13-104">This topic describes how to use the File Type Verifier that is provided in the [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="33d13-105">Si votre programme crée des types de fichiers avec lesquels les utilisateurs sont censés interagir à partir du shell Windows (généralement stocké dans le dossier connu d’un utilisateur tel que **Mes documents**), il est très important de tester votre application et de vérifier que les fichiers qu’elle crée sont correctement enregistrés et de fournir une expérience utilisateur de haute qualité lors de la navigation et de la recherche de fichiers.</span><span class="sxs-lookup"><span data-stu-id="33d13-105">If your program creates file types that users are expected to interact with from the Windows Shell (typically stored in a user's known folder such as **My Documents**), it is very important to test your application and verify that the files it creates are properly registered and provide a high-quality user experience when browsing and searching files.</span></span> <span data-ttu-id="33d13-106">Cela est particulièrement important si vous prévoyez que les utilisateurs exécutent vos applications sur Windows 7, qui s’appuie sur des gestionnaires de types de fichiers de haute qualité pour la plupart des fonctionnalités de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="33d13-106">This is especially important if you expect users to run your applications on Windows 7, which relies on high-quality file type handlers for many of the Shell features.</span></span>

<span data-ttu-id="33d13-107">Pour vérifier votre type de fichier à l’aide du vérificateur de type de fichier, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="33d13-107">To verify your file type using the File Type Verifier, follow these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="33d13-108">Instructions</span><span class="sxs-lookup"><span data-stu-id="33d13-108">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="33d13-109">Étape 1 :</span><span class="sxs-lookup"><span data-stu-id="33d13-109">Step 1:</span></span>

<span data-ttu-id="33d13-110">Installez l’application dans votre environnement de test et copiez le vérificateur de type de fichier dans cet environnement.</span><span class="sxs-lookup"><span data-stu-id="33d13-110">Install the application on your test environment, and copy the File Type Verifier to that environment.</span></span> <span data-ttu-id="33d13-111">Le vérificateur de type de fichier est disponible dans le [Kit de développement logiciel (SDK) Windows 7](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="33d13-111">The File Type Verifier is available in the [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

### <a name="step-2"></a><span data-ttu-id="33d13-112">Étape 2 :</span><span class="sxs-lookup"><span data-stu-id="33d13-112">Step 2:</span></span>

<span data-ttu-id="33d13-113">Utilisez votre application pour créer un fichier à tester.</span><span class="sxs-lookup"><span data-stu-id="33d13-113">Use your application to create a file to be tested.</span></span>

### <a name="step-3"></a><span data-ttu-id="33d13-114">Étape 3 :</span><span class="sxs-lookup"><span data-stu-id="33d13-114">Step 3:</span></span>

<span data-ttu-id="33d13-115">Démarrez le vérificateur de type de fichier.</span><span class="sxs-lookup"><span data-stu-id="33d13-115">Start the File Type Verifier.</span></span>

### <a name="step-4"></a><span data-ttu-id="33d13-116">Étape 4 :</span><span class="sxs-lookup"><span data-stu-id="33d13-116">Step 4:</span></span>

<span data-ttu-id="33d13-117">Sélectionnez la catégorie pour votre type de fichier, comme illustré dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="33d13-117">Select the category for your file type, as shown in the following screen shot.</span></span>

![Capture d’écran montrant la fonction glisser-déplacer.](images/file-assoc/filetypeverifier1.png)

<span data-ttu-id="33d13-119">La sélection de catégorie détermine l’ensemble des tests qui seront exécutés par l’outil.</span><span class="sxs-lookup"><span data-stu-id="33d13-119">The category selection determines the set of tests that will be run by the tool.</span></span> <span data-ttu-id="33d13-120">Si votre type peut appartenir à plusieurs catégories (par exemple, un fichier TIF peut être une image ou un document en fonction du contenu), exécutez à nouveau l’outil avec chaque catégorie appropriée.</span><span class="sxs-lookup"><span data-stu-id="33d13-120">If your type could fall under more than one category (for example, a TIF file might be a Picture or a Document depending on the content), run the tool again with each appropriate category.</span></span>

### <a name="step-5"></a><span data-ttu-id="33d13-121">Étape 5 :</span><span class="sxs-lookup"><span data-stu-id="33d13-121">Step 5:</span></span>

<span data-ttu-id="33d13-122">À l’aide de l’Explorateur Windows, localisez un fichier à tester et utilisez la souris pour le faire glisser vers la cible dans le vérificateur de type de fichier, comme illustré dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="33d13-122">Using Windows Explorer, locate a file to be tested and use the mouse to drag it to the target in File Type Verifier, as shown in the following screen shot.</span></span>

![capture d’écran montrant la fonction glisser-déplacer](images/file-assoc/filetypeverifier2.png)

### <a name="step-6"></a><span data-ttu-id="33d13-124">Étape 6 :</span><span class="sxs-lookup"><span data-stu-id="33d13-124">Step 6:</span></span>

<span data-ttu-id="33d13-125">Attendez que l’outil de vérification de type de fichier parcoure une série de tests.</span><span class="sxs-lookup"><span data-stu-id="33d13-125">Wait for the File Type Verifier tool to proceed through a series of tests.</span></span> <span data-ttu-id="33d13-126">La progression du test est indiquée par la barre de progression, comme dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="33d13-126">The progress of the testing is shown by the progress bar, as in the following screen shot.</span></span>

![capture d’écran montrant la barre de progression](images/file-assoc/filetypeverifier3.png)

### <a name="step-7"></a><span data-ttu-id="33d13-128">Étape 7 :</span><span class="sxs-lookup"><span data-stu-id="33d13-128">Step 7:</span></span>

<span data-ttu-id="33d13-129">Examinez le résumé des résultats de vos tests de type de fichier de document, comme illustré dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="33d13-129">Review the results summary of your Document file type tests, as shown in the following screen shot.</span></span>

![capture d’écran montrant le résumé des résultats](images/file-assoc/filetypeverifier4.png)

### <a name="step-8"></a><span data-ttu-id="33d13-131">Étape 8 :</span><span class="sxs-lookup"><span data-stu-id="33d13-131">Step 8:</span></span>

<span data-ttu-id="33d13-132">Cliquez sur l’un des résultats de la page Résumé pour afficher le journal détaillé.</span><span class="sxs-lookup"><span data-stu-id="33d13-132">Click any of the results on the summary page to view the detailed log.</span></span> <span data-ttu-id="33d13-133">Un exemple de journal pour un gestionnaire d’aperçus est illustré dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="33d13-133">An example log for a preview handler is shown in the following screen shot.</span></span>

![capture d’écran montrant le journal du gestionnaire d’aperçus](images/file-assoc/filetypeverifier5.png)

### <a name="step-9"></a><span data-ttu-id="33d13-135">Étape 9 :</span><span class="sxs-lookup"><span data-stu-id="33d13-135">Step 9:</span></span>

<span data-ttu-id="33d13-136">Pour enregistrer une copie du fichier journal, cliquez sur **enregistrer le fichier journal** en bas de l’affichage du journal et choisissez un emplacement approprié pour le stocker sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="33d13-136">To save a copy of the log file, click **Save Log File** at the bottom of the log display and choose an appropriate location for storing it on your computer.</span></span>

### <a name="step-10"></a><span data-ttu-id="33d13-137">Étape 10 :</span><span class="sxs-lookup"><span data-stu-id="33d13-137">Step 10:</span></span>

<span data-ttu-id="33d13-138">Si des erreurs sont signalées, apportez les modifications appropriées à votre application et réexécutez l’outil pour vérifier que les échecs ne s’afficheront plus dans les tests.</span><span class="sxs-lookup"><span data-stu-id="33d13-138">If failures are reported, make the appropriate changes in your application and run the tool again to verify that the failures are no longer showing up in the tests.</span></span> <span data-ttu-id="33d13-139">Si des avertissements sont signalés, évaluez-les et déterminez s’ils sont pertinents pour votre type de fichier particulier et apportez les modifications appropriées à votre application si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="33d13-139">If warnings are reported, evaluate them and decide whether they are relevant for your particular file type and make the appropriate changes to your application as necessary.</span></span>

## <a name="related-topics"></a><span data-ttu-id="33d13-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="33d13-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33d13-141">Windows 7, SDK</span><span class="sxs-lookup"><span data-stu-id="33d13-141">Windows 7 SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx)
</dt> </dl>

 

 



