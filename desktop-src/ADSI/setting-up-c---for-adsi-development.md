---
title: Configuration de Visual C++ 6,0 pour le développement ADSI
description: Cette rubrique vous montre comment configurer C++ dans Visual Studio afin de pouvoir développer une application ADSI.
ms.assetid: 6f1ab3eb-2e0b-4f3e-b93c-e24c8b3b1a27
ms.tgt_platform: multiple
keywords:
- Configuration de C++ pour le développement ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f2350b88402c921d014b0c93756759a1d0f744
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028550"
---
# <a name="setting-up-visual-c-60-for-adsi-development"></a><span data-ttu-id="50779-104">Configuration de Visual C++ 6,0 pour le développement ADSI</span><span class="sxs-lookup"><span data-stu-id="50779-104">Setting Up Visual C++ 6.0 for ADSI Development</span></span>

<span data-ttu-id="50779-105">Le système de développement Microsoft Visual C++ 6,0 peut être utilisé pour développer des applications d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="50779-105">The Microsoft Visual C++ 6.0 development system can be used to develop enterprise applications.</span></span> <span data-ttu-id="50779-106">Pour configurer votre environnement Visual C++ 6,0 pour développer une application ADSI, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="50779-106">To set up your Visual C++ 6.0 environment to develop an ADSI application, perform the following steps:</span></span>

<span data-ttu-id="50779-107">**Configuration de l’environnement de développement Microsoft Visual C++ 6,0**</span><span class="sxs-lookup"><span data-stu-id="50779-107">**Setting Up the Microsoft Visual C++ 6.0 Development Environment**</span></span>

1.  <span data-ttu-id="50779-108">Pointez sur le répertoire include et la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="50779-108">Point to the include and library directory.</span></span> <span data-ttu-id="50779-109">Sélectionnez **outils \| options**.</span><span class="sxs-lookup"><span data-stu-id="50779-109">Select **Tools \| Options**.</span></span> <span data-ttu-id="50779-110">Cliquez sur l’onglet **répertoire** et spécifiez le chemin d’accès aux fichiers d’en-tête ADSI.</span><span class="sxs-lookup"><span data-stu-id="50779-110">Click the **Directory** tab, and specify the path to the ADSI header files.</span></span>
2.  <span data-ttu-id="50779-111">Incluez le fichier activeds. h dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="50779-111">Include the Activeds.h file in your project.</span></span>
3.  <span data-ttu-id="50779-112">Ajoutez les fichiers activeds. lib et adsiid. lib à l’entrée de l’éditeur de liens pour votre projet.</span><span class="sxs-lookup"><span data-stu-id="50779-112">Add the Activeds.lib and Adsiid.lib files to the linker input for your project.</span></span>
4.  <span data-ttu-id="50779-113">Commencez à programmer avec ADSI.</span><span class="sxs-lookup"><span data-stu-id="50779-113">Begin programming with ADSI.</span></span>

<span data-ttu-id="50779-114">Connectez-vous à un domaine Windows.</span><span class="sxs-lookup"><span data-stu-id="50779-114">Log on to a Windows domain.</span></span> <span data-ttu-id="50779-115">Vous devez également avoir l’autorisation de modifier les données dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="50779-115">You must also have permission to modify data in Active Directory.</span></span> <span data-ttu-id="50779-116">Par défaut, l’administrateur dispose de ce privilège.</span><span class="sxs-lookup"><span data-stu-id="50779-116">By default, the Administrator has this privilege.</span></span> <span data-ttu-id="50779-117">Pour entrer cet exemple de code :</span><span class="sxs-lookup"><span data-stu-id="50779-117">To enter this code example:</span></span>

<span data-ttu-id="50779-118">**Exemple d’application Visual C++ : création d’un utilisateur dans un domaine**</span><span class="sxs-lookup"><span data-stu-id="50779-118">**A Sample Visual C++ Application: Creating a User in a Domain**</span></span>

1.  <span data-ttu-id="50779-119">Démarrez Visual C++ 6,0.</span><span class="sxs-lookup"><span data-stu-id="50779-119">Start Visual C++ 6.0.</span></span>
2.  <span data-ttu-id="50779-120">Créez un projet exécutable autonome.</span><span class="sxs-lookup"><span data-stu-id="50779-120">Create a standalone executable project.</span></span> <span data-ttu-id="50779-121">Il peut s’agir d’une application MFC, ATL ou console.</span><span class="sxs-lookup"><span data-stu-id="50779-121">It can be either an MFC, ATL, or Console Application.</span></span>
3.  <span data-ttu-id="50779-122">Suivez les étapes précédentes pour configurer votre projet.</span><span class="sxs-lookup"><span data-stu-id="50779-122">Follow the previous steps to set up your project.</span></span>
4.  <span data-ttu-id="50779-123">Entrez l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="50779-123">Enter the following code example.</span></span> <span data-ttu-id="50779-124">Remplacez la chaîne « LDAP :As = Users, DC = fabrikam, DC = com » par le chemin ADsPath d’un conteneur dans votre domaine.</span><span class="sxs-lookup"><span data-stu-id="50779-124">Replace the "LDAP://CN=users,DC=fabrikam,DC=com" string with the ADsPath of a container in your domain.</span></span> <span data-ttu-id="50779-125">Vous devez également remplacer le nom d’utilisateur « JeffSmith » par un nom d’utilisateur unique dans votre domaine.</span><span class="sxs-lookup"><span data-stu-id="50779-125">You should also replace the user name "jeffsmith" with a user name that is unique in your domain.</span></span>

    ```C++
    #include "stdafx.h"
    #include "activeds.h"

    int main(int argc, char* argv[])
    {
        HRESULT hr;
        IADsContainer *pCont;
        IDispatch *pDisp=NULL;
        IADs *pUser;

         // Initialize COM before calling any ADSI functions or interfaces.
         CoInitialize(NULL);

        hr = ADsGetObject( L"LDAP://CN=users,DC=fabrikam,DC=com", 
                                   IID_IADsContainer, 
                                   (void**) &pCont );
        
        if ( !SUCCEEDED(hr) )
        {
            return 0;
        }

        //-----------------
        // Create a user
        //-----------------
        
        hr = pCont->Create(CComBSTR("user"), CComBSTR("cn=jeffsmith"), &pDisp );
        
        // Release the container object.    
        pCont->Release();
        
        if ( !SUCCEEDED(hr) )
        {
            return 0;
        }

        hr = pDisp->QueryInterface( IID_IADs, (void**) &pUser );

        // Release the dispatch interface.
        pDisp->Release();

        if ( !SUCCEEDED(hr) )
        {    
            return 0;
        }

        // Commit the object data to the directory.
        pUser->SetInfo();

        // Release the object.
        pUser->Release();

        CoUninitialize();
    }
    ```

    

5.  <span data-ttu-id="50779-126">Générez et exécutez l’application.</span><span class="sxs-lookup"><span data-stu-id="50779-126">Build and run the application.</span></span> <span data-ttu-id="50779-127">Pour vérifier que l’utilisateur a été créé, utilisez l’outil de gestion utilisateurs et ordinateurs Active Directory.</span><span class="sxs-lookup"><span data-stu-id="50779-127">To verify that the user has been created, use the Active Directory Users and Computers management tool.</span></span>

 

 




