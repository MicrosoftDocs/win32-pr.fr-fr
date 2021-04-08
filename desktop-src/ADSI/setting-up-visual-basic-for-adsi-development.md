---
title: Configuration de Visual Basic 6,0 pour le développement ADSI
description: Cette rubrique explique comment configurer Visual Basic dans Visual Studio pour développer une application ADSI.
ms.assetid: 167e89d7-80a3-4cc2-b79c-3744c1b184d6
ms.tgt_platform: multiple
keywords:
- Configuration de Visual Basic pour l’ADSI de développement ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e6b1f39ec06d3716beab750dbf2a522d4c18cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839130"
---
# <a name="setting-up-visual-basic-60-for-adsi-development"></a><span data-ttu-id="4a1ed-104">Configuration de Visual Basic 6,0 pour le développement ADSI</span><span class="sxs-lookup"><span data-stu-id="4a1ed-104">Setting Up Visual Basic 6.0 for ADSI Development</span></span>

<span data-ttu-id="4a1ed-105">**Configuration de l’environnement de développement Microsoft Visual Studio 2010 pour Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="4a1ed-105">**Setting Up the Microsoft Visual Studio 2010 Development Environment For Visual Basic**</span></span>

1.  <span data-ttu-id="4a1ed-106">Démarrez Visual Studio 2010.</span><span class="sxs-lookup"><span data-stu-id="4a1ed-106">Start Visual Studio 2010.</span></span>
2.  <span data-ttu-id="4a1ed-107">Créez un projet de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4a1ed-107">Create a new Visual Basic project.</span></span>
3.  <span data-ttu-id="4a1ed-108">Ajoutez une référence à la **bibliothèque de types Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="4a1ed-108">Add a reference to the **Active DS Type Library**.</span></span>
    > [!Note]  
    > <span data-ttu-id="4a1ed-109">Si vous n’avez pas besoin d’une liaison d’objet COM précoce, ignorez cette étape.</span><span class="sxs-lookup"><span data-stu-id="4a1ed-109">If you do not require early COM object binding, ignore this step.</span></span>

     

    1.  <span data-ttu-id="4a1ed-110">Sélectionnez **projet \| Ajouter une référence**.</span><span class="sxs-lookup"><span data-stu-id="4a1ed-110">Select **Project \| Add Reference**.</span></span>
    2.  <span data-ttu-id="4a1ed-111">Sélectionnez l’onglet **com** .</span><span class="sxs-lookup"><span data-stu-id="4a1ed-111">Select the **COM** tab.</span></span>
    3.  <span data-ttu-id="4a1ed-112">Sélectionnez **bibliothèque de types Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="4a1ed-112">Select **Active DS Type Library**.</span></span>

4.  <span data-ttu-id="4a1ed-113">Commencez à programmer avec ADSI.</span><span class="sxs-lookup"><span data-stu-id="4a1ed-113">Begin programming with ADSI.</span></span>

<span data-ttu-id="4a1ed-114">Avant de commencer, connectez-vous à un domaine Windows.</span><span class="sxs-lookup"><span data-stu-id="4a1ed-114">Before you begin, log on to a Windows domain.</span></span> <span data-ttu-id="4a1ed-115">Vous devez être autorisé à modifier la base de données Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4a1ed-115">You must have permission to modify the Active Directory database.</span></span> <span data-ttu-id="4a1ed-116">Par défaut, l’administrateur dispose de ce privilège.</span><span class="sxs-lookup"><span data-stu-id="4a1ed-116">By default, the Administrator has this privilege.</span></span>

<span data-ttu-id="4a1ed-117">**Exemple d’application Visual Basic 6,0 : modification de FullName et description pour un utilisateur**</span><span class="sxs-lookup"><span data-stu-id="4a1ed-117">**A Sample Visual Basic 6.0 Application: Modifying FullName and Description for a User**</span></span>

1.  <span data-ttu-id="4a1ed-118">Suivez les étapes précédentes pour créer un fichier exécutable standard Visual Basic projet.</span><span class="sxs-lookup"><span data-stu-id="4a1ed-118">Follow the previous steps to create a standard executable Visual Basic project.</span></span>
2.  <span data-ttu-id="4a1ed-119">Double-cliquez sur le formulaire.</span><span class="sxs-lookup"><span data-stu-id="4a1ed-119">Double-click the Form.</span></span> <span data-ttu-id="4a1ed-120">Dans \_ chargement du formulaire, tapez ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="4a1ed-120">In Form\_Load, type the following.</span></span> <span data-ttu-id="4a1ed-121">Vous devez remplacer la chaîne « LDAP : 0408 = JeffSmith, CN = Users, DC = fabrikam, DC = com » par l’ADsPath d’un utilisateur existant dans un conteneur de votre domaine.</span><span class="sxs-lookup"><span data-stu-id="4a1ed-121">You must replace the "LDAP://CN=jeffsmith,CN=users,DC=fabrikam,DC=com" string with the ADsPath of an existing user in a container in your domain.</span></span> <span data-ttu-id="4a1ed-122">Créez un compte d’utilisateur de test qui peut être modifié à cet effet.</span><span class="sxs-lookup"><span data-stu-id="4a1ed-122">Create a test user account that can be modified for this purpose.</span></span>
    ```VB
    '------------------------------------------------------------
    ' This code example is used to set the FullName and Description
    '------------------------------------------------------------
    Dim usr As IADsUser

    ' Bind to a user object.
    Set usr = GetObject("LDAP://CN=jeffsmith,CN=users,DC=fabrikam,DC=com")

    usr.FullName = "Jeff Smith"
    usr.Description = "A user for fabrikam.com" 
    usr.SetInfo ' Commit the changes to the directory
    ```

    

3.  <span data-ttu-id="4a1ed-123">Appuyez sur **<F5>** pour exécuter le programme.</span><span class="sxs-lookup"><span data-stu-id="4a1ed-123">Press **<F5>** to run the program.</span></span>
4.  <span data-ttu-id="4a1ed-124">Pour vérifier les modifications, utilisez l’outil de gestion utilisateurs et ordinateurs Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4a1ed-124">To verify changes, use the Active Directory Users and Computers management tool.</span></span> <span data-ttu-id="4a1ed-125">Pour plus d’informations sur l’utilisation d’ADSI et de Visual Basic, consultez [accès à Active Directory à l’aide de Visual Basic](accessing-active-directory-using-visual-basic.md).</span><span class="sxs-lookup"><span data-stu-id="4a1ed-125">For more information about using ADSI and Visual Basic, see [Accessing Active Directory Using Visual Basic](accessing-active-directory-using-visual-basic.md).</span></span>

 

 




