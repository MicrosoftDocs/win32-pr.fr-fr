---
title: Tests de validation pour les magasins de type 2 en ligne intégrés
description: Cette rubrique décrit les tests que Microsoft effectuera pour valider votre magasin de type 2 en ligne. Microsoft vous demande d’exécuter ces tests avant de soumettre une version Release candidate. Votre magasin en ligne doit réussir à publier ces tests.
ms.assetid: 1da51772-9711-4913-b05d-830fabe49da2
keywords:
- Windows Media Player Online stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beefd0945f9d1a9ae61e61f8be74beada1695baf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379993"
---
# <a name="validation-tests-for-on-boarding-type-2-online-stores"></a><span data-ttu-id="64505-106">Tests de validation pour les magasins de type 2 en ligne intégrés</span><span class="sxs-lookup"><span data-stu-id="64505-106">Validation Tests for On-boarding Type 2 Online Stores</span></span>

<span data-ttu-id="64505-107">Cette rubrique décrit les tests que Microsoft effectuera pour valider votre magasin de type 2 en ligne.</span><span class="sxs-lookup"><span data-stu-id="64505-107">This topic describes tests that Microsoft will perform to validate your Type 2 online store.</span></span> <span data-ttu-id="64505-108">Microsoft vous demande d’exécuter ces tests avant de soumettre une version Release candidate.</span><span class="sxs-lookup"><span data-stu-id="64505-108">Microsoft requires that you run these tests before you submit a release candidate.</span></span> <span data-ttu-id="64505-109">Votre magasin en ligne doit réussir à publier ces tests.</span><span class="sxs-lookup"><span data-stu-id="64505-109">Your online store must successfully pass these tests to be published.</span></span>

> [!Note]  
> <span data-ttu-id="64505-110">Si votre magasin est de type 1 au lieu de type 2, vous pouvez utiliser cette rubrique comme indication pour comprendre l’étendue des tests de certification couverts pour les magasins de type 1.</span><span class="sxs-lookup"><span data-stu-id="64505-110">If your store is Type 1 rather than Type 2, you can use this topic as a guideline to understand the scope of the certification testing that is covered for Type 1 stores.</span></span> <span data-ttu-id="64505-111">Pour l’ensemble complet des tests pour les magasins de type 1, contactez [support Microsoft](https://support.microsoft.com/ph/7763#tab0).</span><span class="sxs-lookup"><span data-stu-id="64505-111">For the complete set of tests for Type 1 stores, contact [Microsoft Support](https://support.microsoft.com/ph/7763#tab0).</span></span>

 

<span data-ttu-id="64505-112">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="64505-112">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="64505-113">Liste de vérification des tests</span><span class="sxs-lookup"><span data-stu-id="64505-113">Test Checklist</span></span>](#test-checklist)
    -   [<span data-ttu-id="64505-114">Préparation de la passe de test</span><span class="sxs-lookup"><span data-stu-id="64505-114">Test Pass Preparation</span></span>](#test-pass-preparation)
-   [<span data-ttu-id="64505-115">Environnement de test</span><span class="sxs-lookup"><span data-stu-id="64505-115">Test Environment</span></span>](#test-environment)
-   [<span data-ttu-id="64505-116">Configuration et installation</span><span class="sxs-lookup"><span data-stu-id="64505-116">Configuration and Setup</span></span>](#configuration-and-setup)
    -   [<span data-ttu-id="64505-117">Configuration d’un ordinateur de test</span><span class="sxs-lookup"><span data-stu-id="64505-117">Setting Up a Test Machine</span></span>](#setting-up-a-test-machine)
    -   [<span data-ttu-id="64505-118">Configuration d’un magasin</span><span class="sxs-lookup"><span data-stu-id="64505-118">Setting Up a Store</span></span>](#setting-up-a-store)
    -   [<span data-ttu-id="64505-119">Création d’un compte</span><span class="sxs-lookup"><span data-stu-id="64505-119">Creating an Account</span></span>](#creating-an-account)
    -   [<span data-ttu-id="64505-120">Configuration de la mise en cache des informations d’identification</span><span class="sxs-lookup"><span data-stu-id="64505-120">Setting Up Credential Caching</span></span>](#setting-up-credential-caching)
-   [<span data-ttu-id="64505-121">Acquisition de contenu</span><span class="sxs-lookup"><span data-stu-id="64505-121">Content Acquisition</span></span>](#content-acquisition)
    -   [<span data-ttu-id="64505-122">Contenu de diffusion en continu</span><span class="sxs-lookup"><span data-stu-id="64505-122">Streaming Content</span></span>](#streaming-content)
    -   [<span data-ttu-id="64505-123">Obtention de contenu</span><span class="sxs-lookup"><span data-stu-id="64505-123">Obtaining Content</span></span>](#obtaining-content)
    -   [<span data-ttu-id="64505-124">Gravage de contenu</span><span class="sxs-lookup"><span data-stu-id="64505-124">Burning Content</span></span>](#burning-content)
    -   [<span data-ttu-id="64505-125">Transfert de contenu</span><span class="sxs-lookup"><span data-stu-id="64505-125">Transferring Content</span></span>](#transferring-content)
-   [<span data-ttu-id="64505-126">Fonctionnalités du Store</span><span class="sxs-lookup"><span data-stu-id="64505-126">Store Features</span></span>](#store-features)
    -   [<span data-ttu-id="64505-127">Gestion d’un compte</span><span class="sxs-lookup"><span data-stu-id="64505-127">Managing an Account</span></span>](#managing-an-account)
    -   [<span data-ttu-id="64505-128">Gestion d’info Center</span><span class="sxs-lookup"><span data-stu-id="64505-128">Managing the Info Center</span></span>](#managing-the-info-center)
-   [<span data-ttu-id="64505-129">Interaction du Store</span><span class="sxs-lookup"><span data-stu-id="64505-129">Store Interaction</span></span>](#store-interaction)
    -   [<span data-ttu-id="64505-130">Donner au magasin actif</span><span class="sxs-lookup"><span data-stu-id="64505-130">Yielding to the Active Store</span></span>](#yielding-to-the-active-store)
    -   [<span data-ttu-id="64505-131">Empêcher le magasin testé de prendre le contrôle du magasin actif</span><span class="sxs-lookup"><span data-stu-id="64505-131">Preventing the Tested Store From Taking Over the Active Store</span></span>](#preventing-the-tested-store-from-taking-over-the-active-store)
    -   [<span data-ttu-id="64505-132">Accès à un magasin en mode High-Contrast</span><span class="sxs-lookup"><span data-stu-id="64505-132">Accessing a Store in High-Contrast Mode</span></span>](#accessing-a-store-in-high-contrast-mode)
    -   [<span data-ttu-id="64505-133">Sécurisation d’un magasin</span><span class="sxs-lookup"><span data-stu-id="64505-133">Securing a Store</span></span>](#securing-a-store)

## <a name="test-checklist"></a><span data-ttu-id="64505-134">Liste de vérification des tests</span><span class="sxs-lookup"><span data-stu-id="64505-134">Test Checklist</span></span>

<span data-ttu-id="64505-135">Utilisez la liste de contrôle figurant dans le tableau suivant pour valider votre boutique en ligne de type 2 que vous souhaitez mettre à l’esprit.</span><span class="sxs-lookup"><span data-stu-id="64505-135">Use the checklist in the following table to validate your Type 2 online store that you wish to bring on board.</span></span>



<span data-ttu-id="64505-136">Test</span><span class="sxs-lookup"><span data-stu-id="64505-136">Test</span></span>

<span data-ttu-id="64505-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="64505-137">Windows XP</span></span>

<span data-ttu-id="64505-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="64505-138">Windows Vista</span></span>

<span data-ttu-id="64505-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="64505-139">Windows 7</span></span>

<span data-ttu-id="64505-140">Résultat (réussite/échec/non applicable)</span><span class="sxs-lookup"><span data-stu-id="64505-140">Result (pass/fail/not applicable)</span></span>

<span data-ttu-id="64505-141">32</span><span class="sxs-lookup"><span data-stu-id="64505-141">32</span></span>

<span data-ttu-id="64505-142">64</span><span class="sxs-lookup"><span data-stu-id="64505-142">64</span></span>

<span data-ttu-id="64505-143">32</span><span class="sxs-lookup"><span data-stu-id="64505-143">32</span></span>

<span data-ttu-id="64505-144">64</span><span class="sxs-lookup"><span data-stu-id="64505-144">64</span></span>

<span data-ttu-id="64505-145">32</span><span class="sxs-lookup"><span data-stu-id="64505-145">32</span></span>

<span data-ttu-id="64505-146">64</span><span class="sxs-lookup"><span data-stu-id="64505-146">64</span></span>

1. <span data-ttu-id="64505-147">Vérifiez que le logiciel est installé.</span><span class="sxs-lookup"><span data-stu-id="64505-147">Verify that software installs.</span></span>

2. <span data-ttu-id="64505-148">Vérifiez que le logiciel est désinstallé.</span><span class="sxs-lookup"><span data-stu-id="64505-148">Verify that software uninstalls.</span></span>

3. <span data-ttu-id="64505-149">Vérifiez que le logiciel ne s’exécute pas dans la barre d’État.</span><span class="sxs-lookup"><span data-stu-id="64505-149">Verify that software does not run in the tray.</span></span>

4. <span data-ttu-id="64505-150">Vérifiez que l’onglet Store fonctionne.</span><span class="sxs-lookup"><span data-stu-id="64505-150">Verify that the store tab operates.</span></span>

5. <span data-ttu-id="64505-151">Vérifiez que le magasin dispose d’une option pour créer un nouveau compte.</span><span class="sxs-lookup"><span data-stu-id="64505-151">Verify that the store has an option to create a new account.</span></span>

6. <span data-ttu-id="64505-152">Vérifiez que le compte créé peut se connecter.</span><span class="sxs-lookup"><span data-stu-id="64505-152">Verify that the created account can sign in.</span></span>

7. <span data-ttu-id="64505-153">Vérifiez que le magasin a une option permettant d’enregistrer les informations utilisateur.</span><span class="sxs-lookup"><span data-stu-id="64505-153">Verify that the store has an option to save user information.</span></span>

8. <span data-ttu-id="64505-154">Vérifiez que la mise en cache des informations d’identification est présente et opérationnelle.</span><span class="sxs-lookup"><span data-stu-id="64505-154">Verify that credential caching is present and working.</span></span>

9. <span data-ttu-id="64505-155">Vérifiez que l’utilisateur est invité à fournir les informations d’identification si elles ne sont pas mises en cache.</span><span class="sxs-lookup"><span data-stu-id="64505-155">Verify that the user is prompted for credentials if they are not cached.</span></span>

10. <span data-ttu-id="64505-156">Vérifiez que tous les types de flux de contenu disponibles.</span><span class="sxs-lookup"><span data-stu-id="64505-156">Verify that all available types of content stream.</span></span>

11. <span data-ttu-id="64505-157">Vérifiez que le contenu est lu dans le lecteur Microsoft Windows Media.</span><span class="sxs-lookup"><span data-stu-id="64505-157">Verify that content plays in Microsoft Windows Media Player.</span></span>

12. <span data-ttu-id="64505-158">Vérifiez que le prix calculé est correct.</span><span class="sxs-lookup"><span data-stu-id="64505-158">Verify that a calculated price is correct.</span></span>

13. <span data-ttu-id="64505-159">Vérifiez que le contenu acheté est téléchargé dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="64505-159">Verify that purchased content is downloaded to the library.</span></span>

14. <span data-ttu-id="64505-160">Vérifiez que les métadonnées sont téléchargées pour l’achat.</span><span class="sxs-lookup"><span data-stu-id="64505-160">Verify that metadata is downloaded for the purchase.</span></span>

15. <span data-ttu-id="64505-161">Vérifiez que les droits d’utilisation du média sont corrects pour l’achat.</span><span class="sxs-lookup"><span data-stu-id="64505-161">Verify that media usage rights are correct for the purchase.</span></span>

16. <span data-ttu-id="64505-162">Vérifiez que le contenu acheté peut être lu.</span><span class="sxs-lookup"><span data-stu-id="64505-162">Verify that the purchased content can play.</span></span>

17. <span data-ttu-id="64505-163">Vérifiez que cliquer sur le bouton **acheter** **ou acheter bascule** sur le Store.</span><span class="sxs-lookup"><span data-stu-id="64505-163">Verify that clicking the **Buy** or **Shop** button switches to the store.</span></span>

18. <span data-ttu-id="64505-164">Vérifiez que le contenu acheté a été téléchargé.</span><span class="sxs-lookup"><span data-stu-id="64505-164">Verify that purchased content downloaded.</span></span>

19. <span data-ttu-id="64505-165">Vérifiez que le contenu acheté peut être gravé.</span><span class="sxs-lookup"><span data-stu-id="64505-165">Verify that purchased content can be burned.</span></span>

20. <span data-ttu-id="64505-166">Vérifiez que le nombre de brûlures est décrémenté.</span><span class="sxs-lookup"><span data-stu-id="64505-166">Verify that the burn count is decremented.</span></span>

21. <span data-ttu-id="64505-167">Vérifiez que le contenu peut être transféré vers un autre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="64505-167">Verify that content can be transferred to another computer.</span></span>

22. <span data-ttu-id="64505-168">Vérifiez que le contenu est transféré vers un appareil.</span><span class="sxs-lookup"><span data-stu-id="64505-168">Verify that content transfers to a device.</span></span>

23. <span data-ttu-id="64505-169">Vérifiez que le nombre de synchronisations est décrémenté.</span><span class="sxs-lookup"><span data-stu-id="64505-169">Verify that the sync count is decremented.</span></span>

24. <span data-ttu-id="64505-170">Vérifiez que l’historique des achats effectue le suivi des achats précédents.</span><span class="sxs-lookup"><span data-stu-id="64505-170">Verify that the purchase history tracks prior purchases.</span></span>

25. <span data-ttu-id="64505-171">Vérifiez qu’un achat précédent peut être restauré.</span><span class="sxs-lookup"><span data-stu-id="64505-171">Verify that a prior purchase can be restored.</span></span>

26. <span data-ttu-id="64505-172">Vérifier la fonctionnalité d’un magasin pour gérer plusieurs ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="64505-172">Verify a store's functionality to manage multiple computers.</span></span>

27. <span data-ttu-id="64505-173">Vérifiez que le centre d’informations est désactivé par défaut.</span><span class="sxs-lookup"><span data-stu-id="64505-173">Verify that the Info Center is off by default.</span></span>

28. <span data-ttu-id="64505-174">Vérifiez que le centre d’informations contient des informations sur le média dans la zone de diffusion en cours.</span><span class="sxs-lookup"><span data-stu-id="64505-174">Verify that the Info Center has media information in the now-playing area.</span></span>

29. <span data-ttu-id="64505-175">Vérifiez que les liens naviguent vers le magasin.</span><span class="sxs-lookup"><span data-stu-id="64505-175">Verify that links navigate to the store.</span></span>

30. <span data-ttu-id="64505-176">Vérifiez que le magasin testé produit le magasin actif.</span><span class="sxs-lookup"><span data-stu-id="64505-176">Verify that the tested store yields to the active store.</span></span>

31. <span data-ttu-id="64505-177">Vérifiez que le magasin testé ne prend pas en charge le magasin actuel.</span><span class="sxs-lookup"><span data-stu-id="64505-177">Verify that the tested store does not take over the current store.</span></span>

32. <span data-ttu-id="64505-178">Vérifiez que le magasin est accessible en mode de contraste élevé.</span><span class="sxs-lookup"><span data-stu-id="64505-178">Verify that the store is accessible in high-contrast mode.</span></span>

33. <span data-ttu-id="64505-179">Vérifiez que le magasin est sécurisé.</span><span class="sxs-lookup"><span data-stu-id="64505-179">Verify that the store is secure.</span></span>



 

### <a name="test-pass-preparation"></a><span data-ttu-id="64505-180">Préparation de la passe de test</span><span class="sxs-lookup"><span data-stu-id="64505-180">Test Pass Preparation</span></span>

<span data-ttu-id="64505-181">Avant d’exécuter un test, vous devez vous assurer que le magasin et les comptes de test sont prêts pour le test.</span><span class="sxs-lookup"><span data-stu-id="64505-181">Before you run a test pass, you should ensure that the store and the test accounts are ready for testing.</span></span> <span data-ttu-id="64505-182">Vous devez déterminer les informations suivantes avant le démarrage de la passe.</span><span class="sxs-lookup"><span data-stu-id="64505-182">You should determine the following information before the pass starts.</span></span> <span data-ttu-id="64505-183">Si vous pouvez déterminer les informations quelques jours avant la réussite du test, la réussite s’exécutera plus efficacement.</span><span class="sxs-lookup"><span data-stu-id="64505-183">If you can determine the information some days in advance of the test pass, the pass will run more efficiently.</span></span>

-   <span data-ttu-id="64505-184">Déterminez les informations suivantes sur les comptes de test qui sont fournis par le magasin :</span><span class="sxs-lookup"><span data-stu-id="64505-184">Determine the following information about test accounts that are supplied by the store:</span></span>
    -   <span data-ttu-id="64505-185">Les comptes et les mots de passe fonctionnent pour permettre à un utilisateur de se connecter</span><span class="sxs-lookup"><span data-stu-id="64505-185">Accounts and passwords work to allow a user to sign in</span></span>
    -   <span data-ttu-id="64505-186">Les comptes sont financés correctement et de manière adéquate pour chaque type de mode d’entreprise proposé par le magasin</span><span class="sxs-lookup"><span data-stu-id="64505-186">Accounts are correctly and adequately funded for each type of business mode the store offers</span></span>
    -   <span data-ttu-id="64505-187">Les comptes sont valides pour tous les paramètres régionaux à tester, ou des comptes existent pour chaque paramètre régional si les comptes ne peuvent pas traverser les paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="64505-187">Accounts are valid for all locales to be tested, or accounts exist for each locale if accounts cannot cross locales</span></span>
-   <span data-ttu-id="64505-188">Déterminez les paramètres régionaux à tester.</span><span class="sxs-lookup"><span data-stu-id="64505-188">Determine which locales to test.</span></span>
-   <span data-ttu-id="64505-189">Déterminez les langues à tester.</span><span class="sxs-lookup"><span data-stu-id="64505-189">Determine which languages to test.</span></span>
-   <span data-ttu-id="64505-190">Déterminez les informations suivantes sur l’environnement de test :</span><span class="sxs-lookup"><span data-stu-id="64505-190">Determine the following information about the test environment:</span></span>

    -   <span data-ttu-id="64505-191">Magasins en direct qui fonctionnent avec Windows XP, Windows Vista et Windows 7</span><span class="sxs-lookup"><span data-stu-id="64505-191">Live stores that work with Windows XP, Windows Vista, and Windows 7</span></span>
    -   <span data-ttu-id="64505-192">Magasin non-Live à tester</span><span class="sxs-lookup"><span data-stu-id="64505-192">The non-live store to test</span></span>
    -   <span data-ttu-id="64505-193">Vérifiez que la Banque non active à tester est visible dans toutes les versions du système d’exploitation et toutes les versions de la plateforme du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="64505-193">Verify that the non-live store to test is visible in all versions of the operating system and all versions of the Windows Media Player platform.</span></span>

-   <span data-ttu-id="64505-194">Déterminez les informations suivantes sur le magasin à tester :</span><span class="sxs-lookup"><span data-stu-id="64505-194">Determine the following information about the store to test:</span></span>

    -   <span data-ttu-id="64505-195">Nom de la banque</span><span class="sxs-lookup"><span data-stu-id="64505-195">Store name</span></span>
    -   <span data-ttu-id="64505-196">Graphiques et étiquette du logo onglet de la boutique ATTENDU</span><span class="sxs-lookup"><span data-stu-id="64505-196">Expected store tab logo graphics and label</span></span>
    -   <span data-ttu-id="64505-197">Le magasin est-il actif pour toutes les versions de système d’exploitation ?</span><span class="sxs-lookup"><span data-stu-id="64505-197">Is the store live for all operating system versions?</span></span>
    -   <span data-ttu-id="64505-198">S’agit-il d’une nouvelle version du magasin testé ?</span><span class="sxs-lookup"><span data-stu-id="64505-198">Is this is a new version of the store under test?</span></span>
    -   <span data-ttu-id="64505-199">Le magasin teste-t-il un magasin de type 1 ou de type 2 ?</span><span class="sxs-lookup"><span data-stu-id="64505-199">Is the store under test a Type 1 or Type 2 store?</span></span>
    -   <span data-ttu-id="64505-200">Le type de magasin a-t-il changé ?</span><span class="sxs-lookup"><span data-stu-id="64505-200">Has the store type changed?</span></span>

-   <span data-ttu-id="64505-201">Déterminez les versions et les plateformes de système d’exploitation pour lesquelles vous envisagez de tester le magasin.</span><span class="sxs-lookup"><span data-stu-id="64505-201">Determine on which operating system versions and platforms you plan to test the store.</span></span>
-   <span data-ttu-id="64505-202">Déterminez que le programme d’installation et le plug-in fonctionnent sur toutes les versions et plateformes du système d’exploitation à tester.</span><span class="sxs-lookup"><span data-stu-id="64505-202">Determine that the installer and plug-in works on all operating system versions and platforms to be tested.</span></span>
-   <span data-ttu-id="64505-203">Déterminez si un document de navigation est requis.</span><span class="sxs-lookup"><span data-stu-id="64505-203">Determine if a navigation document is required.</span></span>
-   <span data-ttu-id="64505-204">Déterminez les informations suivantes sur le support offert par le magasin :</span><span class="sxs-lookup"><span data-stu-id="64505-204">Determine the following information about the media that the store offers:</span></span>

    -   <span data-ttu-id="64505-205">Formats</span><span class="sxs-lookup"><span data-stu-id="64505-205">Formats</span></span>
    -   <span data-ttu-id="64505-206">Tout logiciel propriétaire est-il requis ?</span><span class="sxs-lookup"><span data-stu-id="64505-206">Is any proprietary software required?</span></span>
    -   <span data-ttu-id="64505-207">Devez-vous tester tous les types de média, ou seulement un sous-ensemble de types de média ?</span><span class="sxs-lookup"><span data-stu-id="64505-207">Must you test all media types, or only a subset of media types?</span></span>

-   <span data-ttu-id="64505-208">Déterminez les informations suivantes sur les droits d’utilisation de média :</span><span class="sxs-lookup"><span data-stu-id="64505-208">Determine the following information about media usage rights:</span></span>

    -   <span data-ttu-id="64505-209">Le support de stockage dispose-t-il d’une protection de contenu ?</span><span class="sxs-lookup"><span data-stu-id="64505-209">Does the store media have content protection?</span></span>
    -   <span data-ttu-id="64505-210">Si c’est le cas, déterminez le type de protection de contenu que le média a.</span><span class="sxs-lookup"><span data-stu-id="64505-210">If so, determine the type of content protection that the media have.</span></span>
    -   <span data-ttu-id="64505-211">Si c’est le cas, déterminez le comportement protégé attendu.</span><span class="sxs-lookup"><span data-stu-id="64505-211">If so, determine the expected protected behavior.</span></span>
    -   <span data-ttu-id="64505-212">Les droits d’utilisation des médias incluent-ils le partage d’ordinateur à ordinateur ?</span><span class="sxs-lookup"><span data-stu-id="64505-212">Do the media usage rights include computer-to-computer sharing?</span></span>
    -   <span data-ttu-id="64505-213">Droits de synchronisation</span><span class="sxs-lookup"><span data-stu-id="64505-213">The sync rights</span></span>
    -   <span data-ttu-id="64505-214">Les droits de gravure</span><span class="sxs-lookup"><span data-stu-id="64505-214">The burn rights</span></span>
    -   <span data-ttu-id="64505-215">Droits de lecture</span><span class="sxs-lookup"><span data-stu-id="64505-215">The play rights</span></span>
    -   <span data-ttu-id="64505-216">Dates d’expiration, le cas échéant</span><span class="sxs-lookup"><span data-stu-id="64505-216">The expiration dates, if any</span></span>

-   <span data-ttu-id="64505-217">Déterminez si vous disposez de suffisamment de supports (un grand catalogue) pour fournir un exemple significatif.</span><span class="sxs-lookup"><span data-stu-id="64505-217">Determine if you have sufficient media (a large enough catalog) to provide a meaningful sample.</span></span>
-   <span data-ttu-id="64505-218">Déterminez ce que l’étape passe : RC 0, conformité, etc.</span><span class="sxs-lookup"><span data-stu-id="64505-218">Determine what the stage pass is: RC 0, compliance, and so on.</span></span>
-   <span data-ttu-id="64505-219">Déterminez si la réussite du test est un type particulier : régression, fumée, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="64505-219">Determine if the test pass is a certain type: regression, smoke, and so on.</span></span>

## <a name="test-environment"></a><span data-ttu-id="64505-220">Environnement de test</span><span class="sxs-lookup"><span data-stu-id="64505-220">Test Environment</span></span>

<span data-ttu-id="64505-221">Vous devez procéder à des tests sur les configurations suivantes :</span><span class="sxs-lookup"><span data-stu-id="64505-221">You must conduct testing on the following configurations:</span></span>

-   <span data-ttu-id="64505-222">Systèmes d’exploitation Microsoft Windows Media Player 11 sur Windows XP avec Service Pack 3 (SP3) 32 bits et 64 bits</span><span class="sxs-lookup"><span data-stu-id="64505-222">Microsoft Windows Media Player 11 on Windows XP with Service Pack 3 (SP3) 32-bit and 64-bit operating systems</span></span>
-   <span data-ttu-id="64505-223">Systèmes d’exploitation Windows Media Player 11 sur Windows Vista 32 bits et 64 bits (Windows Media Player 32 bits)</span><span class="sxs-lookup"><span data-stu-id="64505-223">Windows Media Player 11 on Windows Vista 32-bit and 64-bit (32-bit Windows Media Player) operating systems</span></span>
-   <span data-ttu-id="64505-224">Systèmes d’exploitation Microsoft Windows Media Player 12 sur Windows 7 32 bits et 64 bits (Windows Media Player 32 bits)</span><span class="sxs-lookup"><span data-stu-id="64505-224">Microsoft Windows Media Player 12 on Windows 7 32-bit and 64-bit (32-bit Windows Media Player) operating systems</span></span>

<span data-ttu-id="64505-225">Même si vous devez effectuer des tests sur toutes les versions et plateformes du système d’exploitation répertoriées, les versions 32 bits de Windows Vista et Windows 7 sont les versions de système d’exploitation ciblées en priorité.</span><span class="sxs-lookup"><span data-stu-id="64505-225">Although you must perform testing on all the operating system versions and platforms listed, 32-bit versions of Windows Vista and Windows 7 are the priority targeted operating system versions.</span></span> <span data-ttu-id="64505-226">Vous devez tester l’installation de tous les logiciels sur toutes les plateformes.</span><span class="sxs-lookup"><span data-stu-id="64505-226">You must test the installation of any software on all platforms.</span></span>

<span data-ttu-id="64505-227">Les captures d’écran de cette rubrique utilisent un magasin fictif, Proseware, pour illustrer l’utilisation de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="64505-227">Screen shots in this topic use a fictitious store, Proseware, to demonstrate the usage of the user interface.</span></span>

## <a name="configuration-and-setup"></a><span data-ttu-id="64505-228">Configuration et installation</span><span class="sxs-lookup"><span data-stu-id="64505-228">Configuration and Setup</span></span>

<span data-ttu-id="64505-229">Les sections suivantes décrivent comment configurer et configurer un test de validation sur un magasin de type 2 en ligne.</span><span class="sxs-lookup"><span data-stu-id="64505-229">The following sections describe how to configure and set up validation testing to on-board a Type 2 online store.</span></span>

### <a name="setting-up-a-test-machine"></a><span data-ttu-id="64505-230">Configuration d’un ordinateur de test</span><span class="sxs-lookup"><span data-stu-id="64505-230">Setting Up a Test Machine</span></span>

<span data-ttu-id="64505-231">Procédez comme suit pour configurer un ordinateur de test :</span><span class="sxs-lookup"><span data-stu-id="64505-231">Perform the following steps to set up a test machine:</span></span>

1.  <span data-ttu-id="64505-232">Pointez l’ordinateur de test vers les serveurs de test de contenu en ajoutant une clé de Registre spécifique au magasin.</span><span class="sxs-lookup"><span data-stu-id="64505-232">Point the test computer to content test servers by adding a store-specific registry key.</span></span>
2.  <span data-ttu-id="64505-233">Définissez les valeurs de la langue et des paramètres régionaux appropriés dans la boîte de dialogue **Options régionales et linguistiques** .</span><span class="sxs-lookup"><span data-stu-id="64505-233">Set values in the **Regional and Language Options** dialog box to the proper language and locale settings.</span></span> <span data-ttu-id="64505-234">Pour définir la langue, sélectionnez l’onglet **formats** , puis sélectionnez la langue à partir de la zone de liste déroulante **format actuel** .</span><span class="sxs-lookup"><span data-stu-id="64505-234">To set the language, select the **Formats** tab and then select the language from the **Current format** combo box.</span></span> <span data-ttu-id="64505-235">Pour définir la région, sélectionnez l’onglet **emplacement** , puis sélectionnez la région dans la zone de liste déroulante **emplacement actuel** .</span><span class="sxs-lookup"><span data-stu-id="64505-235">To set the region, select the **Location** tab and then select the region from the **Current location** combo box.</span></span> <span data-ttu-id="64505-236">En outre, pour les magasins qui nécessitent l’installation d’un plug-in ou d’un logiciel personnalisé spécifique au magasin, vous devrez peut-être modifier les paramètres régionaux système en fonction de la langue des paramètres régionaux du magasin pour faciliter l’installation.</span><span class="sxs-lookup"><span data-stu-id="64505-236">Additionally, for stores that require installation of a plug-in or store-specific custom software, you might need to change the system locale to the language of the store's locale to facilitate installation.</span></span> <span data-ttu-id="64505-237">Le programme d’installation du logiciel doit prendre en charge les caractères de type simple et double octet et doit s’exécuter sur n’importe quel paramètre régional.</span><span class="sxs-lookup"><span data-stu-id="64505-237">The software installer must support both single and double byte characters and must run on any locale.</span></span> <span data-ttu-id="64505-238">Vous devez tester les paramètres régionaux natifs.</span><span class="sxs-lookup"><span data-stu-id="64505-238">You must test in the native locale.</span></span> <span data-ttu-id="64505-239">Pour définir les paramètres régionaux natifs, ouvrez la boîte de dialogue **région et langue** , sélectionnez l’onglet **administration** , puis cliquez sur le bouton **modifier les paramètres régionaux du système** , comme indiqué dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="64505-239">To set the native locale, open the **Region and Language** dialog box, select the **Administrative** tab, and then click the **Change system locale** button as shown in the following screen shot.</span></span> <span data-ttu-id="64505-240">Cliquez sur ce bouton pour afficher la boîte de dialogue **paramètres régionaux et linguistiques** .</span><span class="sxs-lookup"><span data-stu-id="64505-240">Clicking this button displays the **Region and Language Settings** dialog box.</span></span> <span data-ttu-id="64505-241">La zone de liste déroulante **paramètres régionaux actuels** dans cette boîte de dialogue modifie les paramètres régionaux système.</span><span class="sxs-lookup"><span data-stu-id="64505-241">The **Current system locale** combo box in that dialog box changes the system locale.</span></span>

    <span data-ttu-id="64505-242">Les captures d’écran suivantes montrent les onglets sur lesquels vous pouvez définir la région et la langue :</span><span class="sxs-lookup"><span data-stu-id="64505-242">The following screen shots show the tabs on which you can set region and language:</span></span>

    ![capture d’écran de la boîte de dialogue Options régionales et linguistiques](images/reg-lang-opt.png)

    ![capture d’écran montrant comment modifier les paramètres régionaux du système actuel](images/reg-lang-settings.png)

3.  <span data-ttu-id="64505-245">Désactivez l’affichage du centre d’informations d’un magasin en définissant le lecteur Windows Media pour lire une visualisation.</span><span class="sxs-lookup"><span data-stu-id="64505-245">Turn off the view of a store's Info Center by setting Windows Media Player to play a visualization.</span></span> <span data-ttu-id="64505-246">La principale différence entre les plateformes réside dans le fait que dans le lecteur Windows Media 11, vous commencez par cliquer sur **lecture**, tandis que dans le lecteur Windows Media 12, vous commencez par cliquer avec le bouton droit sur la fenêtre principale.</span><span class="sxs-lookup"><span data-stu-id="64505-246">The main difference between the platforms is that in Windows Media Player 11, you start by clicking **Now Playing**, whereas in Windows Media Player 12, you start by right-clicking the main window.</span></span>

    <span data-ttu-id="64505-247">La capture d’écran suivante montre la séquence d’options de menu qui joue une visualisation dans le lecteur Windows Media 11 :</span><span class="sxs-lookup"><span data-stu-id="64505-247">The following screen shot shows the sequence of menu options that plays a visualization in Windows Media Player 11:</span></span>

    ![capture d’écran montrant comment lire une visualisation dans le lecteur Windows Media 11](images/wmp11-visual.png)

    <span data-ttu-id="64505-249">La capture d’écran suivante montre la séquence d’options de menu qui joue une visualisation dans le lecteur Windows Media 12 :</span><span class="sxs-lookup"><span data-stu-id="64505-249">The following screen shot shows the sequence of menu options that plays a visualization in Windows Media Player 12:</span></span>

    ![capture d’écran montrant comment lire une visualisation dans le lecteur Windows Media 12](images/wmp12-visual.png)

### <a name="setting-up-a-store"></a><span data-ttu-id="64505-251">Configuration d’un magasin</span><span class="sxs-lookup"><span data-stu-id="64505-251">Setting Up a Store</span></span>

<span data-ttu-id="64505-252">Tout d’abord, effectuez les étapes suivantes pour configurer un magasin, puis effectuez les étapes qui suivent les étapes initiales pour vérifier la configuration du magasin :</span><span class="sxs-lookup"><span data-stu-id="64505-252">First perform the following steps to set up a store, and then perform the steps that follow the initial steps to verify the store setup:</span></span>

1.  <span data-ttu-id="64505-253">Lancez le lecteur Windows Media et patientez quelques secondes pour obtenir le dernier fichier de AllServices.xml.</span><span class="sxs-lookup"><span data-stu-id="64505-253">Launch Windows Media Player and wait several seconds to acquire the latest AllServices.xml file.</span></span>
2.  <span data-ttu-id="64505-254">Pour Windows XP et Windows Vista, pour sélectionner un magasin en ligne, cliquez d’abord sur l’onglet qui se divise entre la vue du Guide multimédia et la vue magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="64505-254">For Windows XP and Windows Vista, to select an online store, first click the tab that splits between the Media Guide view and the Online Stores view.</span></span> <span data-ttu-id="64505-255">Ensuite, dans le menu, cliquez sur **parcourir tous les magasins en ligne**, puis sélectionnez le magasin en cliquant sur son icône dans la liste des magasins.</span><span class="sxs-lookup"><span data-stu-id="64505-255">Then, from the menu click **Browse all Online Stores**, and select the store by clicking its icon in the list of stores.</span></span> <span data-ttu-id="64505-256">Pour Windows 7, cliquez sur le bouton dans le volet de navigation de la bibliothèque qui fractionne entre le bouton du **Guide multimédia** et le bouton **magasins en ligne** .</span><span class="sxs-lookup"><span data-stu-id="64505-256">For Windows 7, click the button in the library-navigation pane that splits between the **Media Guide** button and the **Online Stores** button.</span></span> <span data-ttu-id="64505-257">Ensuite, dans le menu, cliquez sur **parcourir tous les magasins en ligne**, puis sélectionnez le magasin en cliquant sur son icône dans la liste des magasins.</span><span class="sxs-lookup"><span data-stu-id="64505-257">Then, from the menu click **Browse all online stores**, and select the store by clicking its icon in the list of stores.</span></span>

    <span data-ttu-id="64505-258">La capture d’écran suivante montre comment sélectionner un magasin en ligne dans le lecteur Windows Media 11 :</span><span class="sxs-lookup"><span data-stu-id="64505-258">The following screen shot shows how to select an online store in Windows Media Player 11:</span></span>

    ![capture d’écran montrant comment sélectionner un magasin en ligne dans le lecteur Windows Media 11](images/wmp11-set-store.png)

    <span data-ttu-id="64505-260">La capture d’écran suivante montre comment sélectionner un magasin en ligne dans le lecteur Windows Media 12 :</span><span class="sxs-lookup"><span data-stu-id="64505-260">The following screen shot shows how to select an Online Store in Windows Media Player 12:</span></span>

    ![capture d’écran montrant comment sélectionner un magasin en ligne dans le lecteur Windows Media 12](images/wmp12-set-store.png)

3.  <span data-ttu-id="64505-262">Suivez les instructions de la boutique pour installer les logiciels supplémentaires nécessaires à l’utilisation du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="64505-262">Follow instructions from the store to install any additional software that is needed to use the store.</span></span>

<span data-ttu-id="64505-263">**Pour vérifier la configuration du magasin**</span><span class="sxs-lookup"><span data-stu-id="64505-263">**To verify store setup**</span></span>

1.  <span data-ttu-id="64505-264">Vérifiez que le logiciel est installé.</span><span class="sxs-lookup"><span data-stu-id="64505-264">Verify that the software installs.</span></span>

    <span data-ttu-id="64505-265">Vérifiez que le plug-in OCX ou tout autre logiciel du Store est téléchargé et installé sans erreur.</span><span class="sxs-lookup"><span data-stu-id="64505-265">Verify that the OCX plug-in or any other software from the store downloads and installs without error.</span></span>

2.  <span data-ttu-id="64505-266">Vérifiez que le logiciel est désinstallé.</span><span class="sxs-lookup"><span data-stu-id="64505-266">Verify that the software uninstalls.</span></span>

    <span data-ttu-id="64505-267">Vérifiez que, dans le panneau de configuration, dans l’élément **programmes et fonctionnalités** , le logiciel que le Store installe apparaît dans la liste **désinstaller ou modifier un programme** , puis vérifiez que vous pouvez le désinstaller de cette liste sans erreur.</span><span class="sxs-lookup"><span data-stu-id="64505-267">Verify that in Control Panel, in the **Programs and Features** item, the software that the store installs appears in the **Uninstall or change a program** list, and verify that you can uninstall it from this list without error.</span></span>

3.  <span data-ttu-id="64505-268">Vérifiez que le logiciel ne s’exécute pas dans la barre d’état système.</span><span class="sxs-lookup"><span data-stu-id="64505-268">Verify that software does not run in the system tray.</span></span>

    <span data-ttu-id="64505-269">Vérifiez qu’aucun des logiciels du Store n’ajoute d’icônes à la zone de notification du programme (dans la barre des tâches à gauche de l’horloge) avant d’avoir donné son consentement au client pour télécharger le logiciel du magasin.</span><span class="sxs-lookup"><span data-stu-id="64505-269">Verify that none of the software from the store adds icons to the program notification area (on the Taskbar to the left of the clock) prior to customer consent to download store software.</span></span>

    <span data-ttu-id="64505-270">L’expérience de base du magasin ne doit pas nécessiter l’installation de logiciels supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="64505-270">The basic store experience should not require installation of additional software.</span></span> <span data-ttu-id="64505-271">Une expérience de base de média, telle que la diffusion de contenu multimédia, doit être disponible.</span><span class="sxs-lookup"><span data-stu-id="64505-271">A basic media experience, such as streaming media, should be available.</span></span> <span data-ttu-id="64505-272">Certains magasins installent des logiciels supplémentaires, tels que les gestionnaires de téléchargement pour une expérience de média premier. ces magasins peuvent avoir des icônes dans la barre d’état système si les icônes représentent des applications distinctes du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="64505-272">Some stores install additional software such as download managers for a premier media experience; these stores can have icons in the system tray if the icons represent applications that are separate from Windows Media Player.</span></span>

4.  <span data-ttu-id="64505-273">Vérifiez que l’onglet Store fonctionne.</span><span class="sxs-lookup"><span data-stu-id="64505-273">Verify that the store tab operates.</span></span>

    <span data-ttu-id="64505-274">Vérifiez que l’onglet Store change pour indiquer le magasin sélectionné.</span><span class="sxs-lookup"><span data-stu-id="64505-274">Verify that the store tab changes to indicate the selected store.</span></span>

    <span data-ttu-id="64505-275">Pour Windows XP et Windows Vista avec le lecteur Windows Media 11, vérifiez que le nom et l’icône de la boutique sont visibles sur l’arrière-plan du lecteur Windows Media 11 sombre.</span><span class="sxs-lookup"><span data-stu-id="64505-275">For Windows XP and Windows Vista with Windows Media Player 11, verify that the store name and icon are visible against the dark Windows Media Player 11 background.</span></span>

    <span data-ttu-id="64505-276">Pour Windows 7 avec le lecteur Windows Media 12, vérifiez que le nom et l’icône du magasin sont visibles dans le volet de navigation de la bibliothèque, dans le menu contextuel du sélecteur de service.</span><span class="sxs-lookup"><span data-stu-id="64505-276">For Windows 7 with Windows Media Player 12, verify the store name and icon are visible in the library-navigation pane, in the service-selector context menu.</span></span>

    <span data-ttu-id="64505-277">Vérifiez que le magasin figure en haut de la liste de sélecteurs de magasin dans le menu.</span><span class="sxs-lookup"><span data-stu-id="64505-277">Verify that the store is listed at the top of the store selector list in the menu.</span></span>

    > [!Note]  
    > <span data-ttu-id="64505-278">Il n’y aura pas **d’option de menu Ajouter le service actuel à** si le magasin de type 2 est le magasin proposé (par défaut) pour la région.</span><span class="sxs-lookup"><span data-stu-id="64505-278">There will be no **Add current service to menu** option if the Type 2 store is the featured (default) store for the region.</span></span>

     

    <span data-ttu-id="64505-279">La capture d’écran suivante montre le menu qui s’affiche lorsque vous cliquez sur l’onglet situé dans le coin supérieur droit du lecteur Windows Media 11 :</span><span class="sxs-lookup"><span data-stu-id="64505-279">The following screen shot shows the menu that appears when you click the tab at the top right corner of Windows Media Player 11:</span></span>

    ![capture d’écran montrant l’onglet Store dans le lecteur Windows Media 11](images/wmp11-verify-store.png)

    <span data-ttu-id="64505-281">La capture d’écran suivante montre le menu qui s’affiche lorsque vous cliquez sur le bouton partagé dans le coin inférieur gauche du lecteur Windows Media 12 :</span><span class="sxs-lookup"><span data-stu-id="64505-281">The following screen shot shows the menu that appears when you click the split button at the lower left corner of Windows Media Player 12:</span></span>

    ![capture d’écran montrant l’onglet Store dans le lecteur Windows Media 12](images/wmp12-verify-store.png)

### <a name="creating-an-account"></a><span data-ttu-id="64505-283">Création d’un compte</span><span class="sxs-lookup"><span data-stu-id="64505-283">Creating an Account</span></span>

<span data-ttu-id="64505-284">**Pour vérifier la configuration du compte**</span><span class="sxs-lookup"><span data-stu-id="64505-284">**To verify account setup**</span></span>

1.  <span data-ttu-id="64505-285">Vérifiez que le magasin dispose d’une option pour créer un nouveau compte, puis suivez les instructions du magasin pour créer un nouveau compte.</span><span class="sxs-lookup"><span data-stu-id="64505-285">Verify that the store has an option to create a new account, and then follow the store instructions to create a new account.</span></span>

    <span data-ttu-id="64505-286">La capture d’écran suivante met en surbrillance un bouton **créer un nouveau compte** tel qu’il peut apparaître dans le lecteur Windows Media 11 :</span><span class="sxs-lookup"><span data-stu-id="64505-286">The following screen shot highlights a **Create New Account** button as it might appear in Windows Media Player 11:</span></span>

    ![capture d’écran montrant comment vérifier la configuration de compte pour le lecteur Windows Media 11](images/wmp11-verify-account.png)

    <span data-ttu-id="64505-288">La capture d’écran suivante met en surbrillance un bouton **créer un nouveau compte** tel qu’il peut apparaître dans le lecteur Windows Media 12 :</span><span class="sxs-lookup"><span data-stu-id="64505-288">The following screen shot highlights a **Create New Account** button as it might appear in Windows Media Player 12:</span></span>

    ![capture d’écran montrant comment vérifier la configuration de compte pour le lecteur Windows Media 12](images/wmp12-verify-account.png)

2.  <span data-ttu-id="64505-290">Vérifiez que vous pouvez vous connecter au compte que vous avez créé.</span><span class="sxs-lookup"><span data-stu-id="64505-290">Verify that you can sign in to the account that you created.</span></span>

### <a name="setting-up-credential-caching"></a><span data-ttu-id="64505-291">Configuration de la mise en cache des informations d’identification</span><span class="sxs-lookup"><span data-stu-id="64505-291">Setting Up Credential Caching</span></span>

<span data-ttu-id="64505-292">Tout d’abord, procédez comme suit pour configurer la mise en cache des informations d’identification, puis effectuez les étapes qui suivent les étapes initiales pour vérifier la configuration de la mise en cache des informations d’identification :</span><span class="sxs-lookup"><span data-stu-id="64505-292">First perform the following steps to set up credential caching, and then perform the steps that follow the initial steps to verify the credential-caching setup:</span></span>

1.  <span data-ttu-id="64505-293">Sur la page de connexion, entrez les informations d’identification et sélectionnez l’option permettant d’enregistrer les informations utilisateur.</span><span class="sxs-lookup"><span data-stu-id="64505-293">At the sign-in page, enter credentials and select the option to save user information.</span></span>
2.  <span data-ttu-id="64505-294">Vérifiez que la page de connexion a une case à cocher qui permet à l’utilisateur de mettre en cache les informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="64505-294">Verify that the sign-in page has a check box that allows the user to cache credentials.</span></span>
3.  <span data-ttu-id="64505-295">La mise en cache facultative des informations d’identification est un point de sécurité important.</span><span class="sxs-lookup"><span data-stu-id="64505-295">Optional credential caching is an important security point.</span></span> <span data-ttu-id="64505-296">La mise en cache automatique des informations d’identification peut exposer des informations d’identification personnelle des utilisateurs qui se connectent à un ordinateur public ou partagé.</span><span class="sxs-lookup"><span data-stu-id="64505-296">Automatic credential caching can expose personally identifiable information of users who sign into a shared or public computer.</span></span> <span data-ttu-id="64505-297">Vous devez protéger les informations client en proposant une case à cocher qui rend la mise en cache facultative.</span><span class="sxs-lookup"><span data-stu-id="64505-297">You should protect customer information by offering a check box that renders the caching optional.</span></span>

<span data-ttu-id="64505-298">**Pour vérifier la mise en cache des informations d’identification**</span><span class="sxs-lookup"><span data-stu-id="64505-298">**To verify credential caching**</span></span>

1.  <span data-ttu-id="64505-299">Vérifiez que le magasin possède une case à cocher pour une option **enregistrer mes informations utilisateur** .</span><span class="sxs-lookup"><span data-stu-id="64505-299">Verify that the store has a check box for a **Save my user information** option.</span></span>

    1.  <span data-ttu-id="64505-300">Fermez le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="64505-300">Close Windows Media Player.</span></span>
    2.  <span data-ttu-id="64505-301">Rouvrez le lecteur Windows Media et essayez de télécharger du contenu.</span><span class="sxs-lookup"><span data-stu-id="64505-301">Reopen Windows Media Player and attempt to download some content.</span></span>

2.  <span data-ttu-id="64505-302">Vérifiez que la mise en cache des informations d’identification est présente et opérationnelle.</span><span class="sxs-lookup"><span data-stu-id="64505-302">Verify that credential caching is present and working.</span></span>

    1.  <span data-ttu-id="64505-303">Déconnectez-vous du Store.</span><span class="sxs-lookup"><span data-stu-id="64505-303">Sign out of the store.</span></span>
    2.  <span data-ttu-id="64505-304">Fermez le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="64505-304">Close Windows Media Player.</span></span>
    3.  <span data-ttu-id="64505-305">Rouvrez le lecteur Windows Media et essayez de télécharger du contenu.</span><span class="sxs-lookup"><span data-stu-id="64505-305">Reopen Windows Media Player and attempt to download some content.</span></span>

3.  <span data-ttu-id="64505-306">Vérifiez que l’utilisateur est invité à fournir les informations d’identification si elles ne sont pas mises en cache.</span><span class="sxs-lookup"><span data-stu-id="64505-306">Verify that the user is prompted for credentials if they are not cached.</span></span>

    <span data-ttu-id="64505-307">Après la déconnexion, puis la tentative d’utilisation du magasin, le client doit être invité à fournir des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="64505-307">After signing out and then trying to use the store, the customer should be prompted for credentials.</span></span>

## <a name="content-acquisition"></a><span data-ttu-id="64505-308">Acquisition de contenu</span><span class="sxs-lookup"><span data-stu-id="64505-308">Content Acquisition</span></span>

<span data-ttu-id="64505-309">Cette section décrit les différentes façons d’acquérir du contenu et comment vérifier que le contenu a été acquis.</span><span class="sxs-lookup"><span data-stu-id="64505-309">This section describes the various ways to acquire content and how to verify that that content was acquired.</span></span>

### <a name="streaming-content"></a><span data-ttu-id="64505-310">Contenu de diffusion en continu</span><span class="sxs-lookup"><span data-stu-id="64505-310">Streaming Content</span></span>

<span data-ttu-id="64505-311">Diffuse tous les types de contenu disponibles à partir du magasin.</span><span class="sxs-lookup"><span data-stu-id="64505-311">Stream all available types of content from the store.</span></span> <span data-ttu-id="64505-312">Par exemple, diffuser en continu le contenu radio, vidéo, audio et aperçu.</span><span class="sxs-lookup"><span data-stu-id="64505-312">For example, stream radio, video, audio, and previews content.</span></span>

<span data-ttu-id="64505-313">**Pour vérifier le contenu de diffusion en continu**</span><span class="sxs-lookup"><span data-stu-id="64505-313">**To verify streaming content**</span></span>

1.  <span data-ttu-id="64505-314">Vérifiez que tous les types de flux de contenu disponibles.</span><span class="sxs-lookup"><span data-stu-id="64505-314">Verify that all available types of content stream.</span></span>

2.  <span data-ttu-id="64505-315">Vérifiez que le contenu est lu dans le lecteur Windows Media et non dans un autre lecteur ou contrôle.</span><span class="sxs-lookup"><span data-stu-id="64505-315">Verify that content plays in Windows Media Player and not some other player or control.</span></span>

### <a name="obtaining-content"></a><span data-ttu-id="64505-316">Obtention de contenu</span><span class="sxs-lookup"><span data-stu-id="64505-316">Obtaining Content</span></span>

<span data-ttu-id="64505-317">Tout d’abord, effectuez les étapes suivantes pour acheter du contenu, puis effectuez les étapes qui suivent les étapes initiales pour vérifier l’achat et vérifier que le contenu a été téléchargé :</span><span class="sxs-lookup"><span data-stu-id="64505-317">First perform the following steps to purchase content, and then perform the steps that follow the initial steps to verify the purchase and verify that the content downloaded:</span></span>

1.  <span data-ttu-id="64505-318">Lancez le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="64505-318">Launch Windows Media Player.</span></span>
2.  <span data-ttu-id="64505-319">Connectez-vous au compte de test.</span><span class="sxs-lookup"><span data-stu-id="64505-319">Sign in to the test account.</span></span>
3.  <span data-ttu-id="64505-320">Accédez au contenu à acheter.</span><span class="sxs-lookup"><span data-stu-id="64505-320">Navigate to the content to purchase.</span></span>
4.  <span data-ttu-id="64505-321">Suivez la procédure spécifique au magasin pour acheter du contenu.</span><span class="sxs-lookup"><span data-stu-id="64505-321">Follow the store-specific procedure to purchase content.</span></span>

<span data-ttu-id="64505-322">**Pour vérifier le contenu acheté et téléchargé**</span><span class="sxs-lookup"><span data-stu-id="64505-322">**To verify purchased and downloaded content**</span></span>

1.  <span data-ttu-id="64505-323">Vérifiez que le prix calculé est correct.</span><span class="sxs-lookup"><span data-stu-id="64505-323">Verify that the calculated price is correct.</span></span>

    <span data-ttu-id="64505-324">Vérifiez que le prix est correct, en particulier lors de l’achat de plusieurs éléments de contenu à la fois, et vérifiez que les informations de solde du compte sont mises à jour correctement après l’achat.</span><span class="sxs-lookup"><span data-stu-id="64505-324">Verify that the price is correct, especially when purchasing multiple pieces of content at once, and verify that any account balance information is updated correctly after purchase.</span></span> <span data-ttu-id="64505-325">Certains contenus peuvent être achetés en tant que pistes uniques et en tant qu’albums uniquement.</span><span class="sxs-lookup"><span data-stu-id="64505-325">Some content can be purchased as single tracks and some as albums only.</span></span> <span data-ttu-id="64505-326">Vérifiez que le prix de l’album n’est pas supérieur à la somme des pistes individuelles.</span><span class="sxs-lookup"><span data-stu-id="64505-326">Verify that the album price is not larger than the sum of the individual tracks.</span></span>

2.  <span data-ttu-id="64505-327">Vérifiez que le contenu acheté est téléchargé dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="64505-327">Verify that the purchased content downloads to the library.</span></span>

    <span data-ttu-id="64505-328">Une fois le téléchargement terminé, accédez au contenu téléchargé dans la bibliothèque du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="64505-328">When the download completes, navigate to the downloaded content in the Windows Media Player library.</span></span> <span data-ttu-id="64505-329">Le contenu téléchargé se trouve dans la bibliothèque de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="64505-329">The downloaded content is located in the current user's library.</span></span>

    -   <span data-ttu-id="64505-330">Pour Windows XP et Windows Vista avec le lecteur Windows Media 11, le contenu téléchargé s’affiche dans le volet de navigation de la bibliothèque, sous **bibliothèque** pivot, puis sous **chansons**.</span><span class="sxs-lookup"><span data-stu-id="64505-330">For Windows XP and Windows Vista with Windows Media Player 11, downloaded content appears in the library navigation pane, under **Library** pivot, and then under **Songs**.</span></span>
    -   <span data-ttu-id="64505-331">Pour Windows 7 avec le lecteur Windows Media 12, le contenu téléchargé dans la bibliothèque du lecteur Windows Media s’affiche dans le volet de navigation du lecteur Windows Media sous **musique**.</span><span class="sxs-lookup"><span data-stu-id="64505-331">For Windows 7 with Windows Media Player 12, content that is downloaded to the Windows Media Player library appears in the Windows Media Player navigation pane under **Music**.</span></span>

3.  <span data-ttu-id="64505-332">Vérifiez que les métadonnées sont téléchargées pour l’achat.</span><span class="sxs-lookup"><span data-stu-id="64505-332">Verify that metadata downloads for the purchase.</span></span>

    <span data-ttu-id="64505-333">Vérifiez que les colonnes suivantes s’affichent dans la bibliothèque du lecteur Windows Media (ajoutez-les si ce n’est pas le cas) :</span><span class="sxs-lookup"><span data-stu-id="64505-333">Ensure that the following columns appear in the Windows Media Player library (add them if not):</span></span>

    -   <span data-ttu-id="64505-334">Artiste de l’album</span><span class="sxs-lookup"><span data-stu-id="64505-334">Album Artist</span></span>
    -   <span data-ttu-id="64505-335">Intitulé</span><span class="sxs-lookup"><span data-stu-id="64505-335">Title</span></span>
    -   <span data-ttu-id="64505-336">Titre de l’album</span><span class="sxs-lookup"><span data-stu-id="64505-336">Album Title</span></span>
    -   <span data-ttu-id="64505-337">Fournisseur de contenu</span><span class="sxs-lookup"><span data-stu-id="64505-337">Content Provider</span></span>
    -   <span data-ttu-id="64505-338">Genre</span><span class="sxs-lookup"><span data-stu-id="64505-338">Genre</span></span>

    <span data-ttu-id="64505-339">Les colonnes précédentes doivent être remplies.</span><span class="sxs-lookup"><span data-stu-id="64505-339">The preceding columns must be populated.</span></span> <span data-ttu-id="64505-340">Le contenu doit avoir une pochette d’album.</span><span class="sxs-lookup"><span data-stu-id="64505-340">Content should have album art.</span></span> <span data-ttu-id="64505-341">Toutefois, une pochette d’album n’est pas nécessaire pour réussir le test de validation.</span><span class="sxs-lookup"><span data-stu-id="64505-341">However, album art is not required to pass validation testing.</span></span>

4.  <span data-ttu-id="64505-342">Vérifiez que les droits d’utilisation du média sont corrects pour l’achat.</span><span class="sxs-lookup"><span data-stu-id="64505-342">Verify that media usage rights are correct for the purchase.</span></span>

    <span data-ttu-id="64505-343">Pour chaque piste téléchargée, cliquez avec le bouton droit sur la piste et sélectionnez **Propriétés**, puis sélectionnez l’onglet **droits d’utilisation du média** .</span><span class="sxs-lookup"><span data-stu-id="64505-343">For each downloaded track, right-click the track and select **Properties**, and then select the **Media Usage Rights** tab.</span></span>

    <span data-ttu-id="64505-344">Le magasin peut choisir de protéger son contenu avec des droits d’utilisation de média, ou choisir de ne pas protéger le contenu.</span><span class="sxs-lookup"><span data-stu-id="64505-344">The store can choose to protect its content with media usage rights, or can choose to not protect the content.</span></span> <span data-ttu-id="64505-345">L’onglet **droits d’utilisation du média** reflète cet État en répertoriant les restrictions ou en indiquant que le contenu n’est pas protégé.</span><span class="sxs-lookup"><span data-stu-id="64505-345">The **Media Usage Rights** tab reflects that status either by listing the restrictions, or by stating that the content is not protected.</span></span> <span data-ttu-id="64505-346">Le magasin doit communiquer son plan le plus récent pour les droits d’utilisation du support.</span><span class="sxs-lookup"><span data-stu-id="64505-346">The store must communicate its most current plan for media usage rights.</span></span> <span data-ttu-id="64505-347">Vous devez vérifier les résultats réels par rapport à ce comportement attendu.</span><span class="sxs-lookup"><span data-stu-id="64505-347">You must verify actual results against this expected behavior.</span></span>

    <span data-ttu-id="64505-348">Les licences de droits de support doivent être pré-remises.</span><span class="sxs-lookup"><span data-stu-id="64505-348">Media rights licenses must be pre-delivered.</span></span> <span data-ttu-id="64505-349">Le client ne doit pas être obligé de lire le contenu ou de passer par un autre processus pour bénéficier de la licence.</span><span class="sxs-lookup"><span data-stu-id="64505-349">The customer must not be required to play the content or go through some other process to get the license.</span></span> <span data-ttu-id="64505-350">Vous devez comparer les droits d’utilisation de médias spécifiques à ce que le magasin a communiqué au client, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="64505-350">You must compare the specific media usage rights to what the store has communicated to the customer as appropriate.</span></span> <span data-ttu-id="64505-351">Les droits doivent pouvoir être transférés sur au moins deux autres ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="64505-351">Rights must be transferable to at least two other computers.</span></span> <span data-ttu-id="64505-352">Les clients doivent être en mesure de graver et de synchroniser leurs médias.</span><span class="sxs-lookup"><span data-stu-id="64505-352">Customers must be able to burn and synchronize their media.</span></span>

    <span data-ttu-id="64505-353">La capture d’écran suivante montre les droits d’utilisation du média d’un fichier protégé :</span><span class="sxs-lookup"><span data-stu-id="64505-353">The following screen shot shows the media usage rights of a protected file:</span></span>

    ![capture d’écran montrant les droits d’utilisation de média pour un fichier protégé](images/media-rights-protected.png)

    <span data-ttu-id="64505-355">Si le contenu n’est pas protégé, l’onglet **droits d’utilisation du média** indique ce fait.</span><span class="sxs-lookup"><span data-stu-id="64505-355">If the content is not protected, the **Media Usage Rights** tab indicates this fact.</span></span>

    <span data-ttu-id="64505-356">La capture d’écran suivante montre les droits d’utilisation du média d’un fichier non protégé :</span><span class="sxs-lookup"><span data-stu-id="64505-356">The following screen shot shows the media usage rights of an unprotected file:</span></span>

    ![capture d’écran montrant les droits d’utilisation de média pour un fichier non protégé](images/media-rights-not-protected.png)

5.  <span data-ttu-id="64505-358">Vérifiez que le contenu acheté est lu.</span><span class="sxs-lookup"><span data-stu-id="64505-358">Verify that the purchased content plays.</span></span>

    <span data-ttu-id="64505-359">Vérifiez que le contenu téléchargé est lu dans le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="64505-359">Verify that downloaded content plays in Windows Media Player.</span></span>

    <span data-ttu-id="64505-360">Lire tout contenu acheté dans le magasin et qui réside dans la bibliothèque locale, ou diffuser un aperçu.</span><span class="sxs-lookup"><span data-stu-id="64505-360">Play any content that was purchased from the store and that resides in the local library, or stream a preview.</span></span>

    <span data-ttu-id="64505-361">Pour acheter du contenu dans Windows XP et Windows Vista avec le lecteur Windows Media 11, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="64505-361">Perform the following steps to purchase content in Windows XP and Windows Vista with Windows Media Player 11:</span></span>

    1.  <span data-ttu-id="64505-362">Cliquez sur l’onglet en **cours de diffusion** .</span><span class="sxs-lookup"><span data-stu-id="64505-362">Click the **Now Playing** tab.</span></span>
    2.  <span data-ttu-id="64505-363">Dans le volet liste, positionnez le pointeur de la souris pour pointer sur une pochette d’album afin d’afficher le lien d' **achat** .</span><span class="sxs-lookup"><span data-stu-id="64505-363">In the list pane, position the mouse pointer to hover over album art in order to show the **Buy** link.</span></span>
    3.  <span data-ttu-id="64505-364">Cliquez sur **acheter**.</span><span class="sxs-lookup"><span data-stu-id="64505-364">Click **Buy**.</span></span>

    <span data-ttu-id="64505-365">La capture d’écran suivante montre l’emplacement du lien d' **achat** dans le lecteur Windows Media 11 :</span><span class="sxs-lookup"><span data-stu-id="64505-365">The following screen shot shows the location of the **Buy** link in Windows Media Player 11:</span></span>

    ![capture d’écran montrant comment acheter du contenu dans le lecteur Windows Media 11](images/wmp11-verify-buy-play.png)

    <span data-ttu-id="64505-367">Pour acheter du contenu dans Windows 7 avec le lecteur Windows Media 12, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="64505-367">Perform the following steps to purchase content in Windows 7 with Windows Media Player 12:</span></span>

    1.  <span data-ttu-id="64505-368">En mode bibliothèque, cliquez sur l’onglet **lecture** .</span><span class="sxs-lookup"><span data-stu-id="64505-368">In library mode, click the **Play** tab.</span></span>
    2.  <span data-ttu-id="64505-369">Dans la sélection, sous la pochette de l’album, cliquez sur **acheter**</span><span class="sxs-lookup"><span data-stu-id="64505-369">In the playlist, under the album art, click **Shop**</span></span>

    <span data-ttu-id="64505-370">La capture d’écran suivante montre comment acheter du contenu dans le lecteur Windows Media 12 :</span><span class="sxs-lookup"><span data-stu-id="64505-370">The following screen shot shows how to buy content in Windows Media Player 12:</span></span>

    ![capture d’écran montrant comment acheter du contenu dans le lecteur Windows Media 12](images/wmp12-verify-buy-play.png)

6.  <span data-ttu-id="64505-372">Vérifiez que le fait de cliquer sur **acheter** **ou acheter** bascule dans le Store.</span><span class="sxs-lookup"><span data-stu-id="64505-372">Verify that clicking **Buy** or **Shop** switches to the store.</span></span>

    <span data-ttu-id="64505-373">Le lecteur Windows Media doit basculer vers le Store dans la vue Bibliothèque et charger l’expérience d’achat du magasin.</span><span class="sxs-lookup"><span data-stu-id="64505-373">The Windows Media Player should switch to the store in library view and load the purchasing experience of the store.</span></span>

    <span data-ttu-id="64505-374">Vous devez ensuite continuer à acheter le suivi.</span><span class="sxs-lookup"><span data-stu-id="64505-374">You must then continue to purchase the track.</span></span>

7.  <span data-ttu-id="64505-375">Après avoir cliqué sur **acheter** ou **acheter**, vérifiez que le contenu est téléchargé.</span><span class="sxs-lookup"><span data-stu-id="64505-375">Verify that after clicking **Buy** or **Shop**, the content downloads.</span></span>

    <span data-ttu-id="64505-376">Vérifiez que les droits d’utilisation du média sont appropriés pour le contenu acheté et ses métadonnées, et vérifiez que la piste est lue.</span><span class="sxs-lookup"><span data-stu-id="64505-376">Verify that the media usage rights are appropriate for the purchased content and its metadata, and verify that the track plays.</span></span> <span data-ttu-id="64505-377">En général, cette méthode d’achat doit avoir les mêmes résultats que les autres méthodes.</span><span class="sxs-lookup"><span data-stu-id="64505-377">In general, this method of purchase should have the same results as other methods.</span></span>

### <a name="burning-content"></a><span data-ttu-id="64505-378">Gravage de contenu</span><span class="sxs-lookup"><span data-stu-id="64505-378">Burning Content</span></span>

<span data-ttu-id="64505-379">Tout d’abord, effectuez les étapes suivantes pour graver du contenu acheté (copier le contenu acheté sur un CD ou DVD inscriptible), puis effectuez les étapes qui suivent les étapes initiales pour vérifier que le contenu est en cours de gravure :</span><span class="sxs-lookup"><span data-stu-id="64505-379">First perform the following steps to burn purchased content (copy purchased content to a writeable CD or DVD), and then perform the steps that follow the initial steps to verify that the content burns:</span></span>

> [!Note]  
> <span data-ttu-id="64505-380">Avant de graver une piste achetée, notez son nombre de brûlures afin de pouvoir vérifier ultérieurement si le nombre est décrémenté après avoir gravé la piste.</span><span class="sxs-lookup"><span data-stu-id="64505-380">Before you burn a purchased track, note its burn count so you can later verify whether the count decrements after you burn the track.</span></span>

 

1.  <span data-ttu-id="64505-381">Cliquez sur l’onglet **graver**</span><span class="sxs-lookup"><span data-stu-id="64505-381">Click the **Burn** tab</span></span>
2.  <span data-ttu-id="64505-382">Faites glisser les pistes achetées vers la **liste de gravure**.</span><span class="sxs-lookup"><span data-stu-id="64505-382">Drag purchased tracks to the **Burn List**.</span></span>
3.  <span data-ttu-id="64505-383">Cliquez sur le bouton **Démarrer la gravure** .</span><span class="sxs-lookup"><span data-stu-id="64505-383">Click the **Start Burn** button.</span></span>

<span data-ttu-id="64505-384">La capture d’écran suivante montre la **liste de gravure** sur le côté droit de l’écran et le bouton Démarrer la **gravure** sous la liste de **gravure** dans le lecteur Windows Media 11 :</span><span class="sxs-lookup"><span data-stu-id="64505-384">The following screen shot shows the **Burn List** on the right side of the screen and the **Start Burn** button below the **Burn List** in Windows Media Player 11:</span></span>

![capture d’écran montrant comment graver du contenu dans le lecteur Windows Media 11](images/wmp11-verify-burn.png)

<span data-ttu-id="64505-386">La capture d’écran suivante montre comment la liste de gravure s’affiche dans le lecteur Windows Media 12 après avoir fait glisser une piste vers la liste de gravure et affiche le bouton **Démarrer la gravure** en haut de l’onglet **graver** :</span><span class="sxs-lookup"><span data-stu-id="64505-386">The following screen shot shows how the burn list appears in Windows Media Player 12 after you drag a track to the burn list, and it shows the **Start Burn** button at the top of the **Burn** tab:</span></span>

![capture d’écran montrant comment graver du contenu dans le lecteur Windows Media 12](images/wmp12-verify-burn.png)

<span data-ttu-id="64505-388">**Pour vérifier que le contenu acheté peut être gravé**</span><span class="sxs-lookup"><span data-stu-id="64505-388">**To verify that purchased content can be burned**</span></span>

1.  <span data-ttu-id="64505-389">Vérifiez que le contenu acheté émet des brûlures en lisant le CD ou le DVD une fois la gravure terminée.</span><span class="sxs-lookup"><span data-stu-id="64505-389">Verify that the purchased content burns by playing the CD or DVD after burning completes.</span></span>

2.  <span data-ttu-id="64505-390">Vérifiez que le nombre de brûlures est décrémenté.</span><span class="sxs-lookup"><span data-stu-id="64505-390">Verify that the burn count is decremented.</span></span>

    <span data-ttu-id="64505-391">Accédez à la bibliothèque et ouvrez les droits d’utilisation de support pour une piste achetée qui a été gravée.</span><span class="sxs-lookup"><span data-stu-id="64505-391">Navigate to the library and open the media usage rights for a purchased track that was burned.</span></span>

    <span data-ttu-id="64505-392">Si le nombre de fois qu’une piste peut être gravée est limité, vérifiez que ce nombre diminue après la gravure de la piste.</span><span class="sxs-lookup"><span data-stu-id="64505-392">If the number of times a track can be burned is limited, verify that this number decreases after the track is burned.</span></span>

### <a name="transferring-content"></a><span data-ttu-id="64505-393">Transfert de contenu</span><span class="sxs-lookup"><span data-stu-id="64505-393">Transferring Content</span></span>

<span data-ttu-id="64505-394">Transférer du contenu vers un autre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="64505-394">Transfer content to another computer.</span></span>

<span data-ttu-id="64505-395">**Pour vérifier que le contenu acheté peut être transféré vers un autre ordinateur**</span><span class="sxs-lookup"><span data-stu-id="64505-395">**To verify that purchased content can be transferred to another computer**</span></span>

-   <span data-ttu-id="64505-396">Si le magasin autorise le transfert de contenu vers un autre ordinateur, transférez le contenu sur au moins deux ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="64505-396">If the store allows transferring content to another computer, transfer the content to at least two computers.</span></span>

<span data-ttu-id="64505-397">Tout d’abord, effectuez les étapes suivantes pour synchroniser sur un appareil et transférer le contenu acheté sur cet appareil, puis effectuez les étapes qui suivent les étapes initiales pour vérifier que le contenu est transféré :</span><span class="sxs-lookup"><span data-stu-id="64505-397">First perform the following steps to sync to a device and transfer purchased content to that device, and then perform the steps that follow the initial steps to verify that the content is transferred:</span></span>

> [!Note]  
> <span data-ttu-id="64505-398">Avant de transférer une piste achetée, notez son nombre de synchronisation afin de pouvoir vérifier ultérieurement si le nombre est décrémenté après le transfert de la piste.</span><span class="sxs-lookup"><span data-stu-id="64505-398">Before you transfer a purchased track, note its sync count so you can later verify whether the count decrements after you transfer the track.</span></span>

 

1.  <span data-ttu-id="64505-399">Connectez un appareil avec une horloge sécurisée.</span><span class="sxs-lookup"><span data-stu-id="64505-399">Connect a device with a secure clock.</span></span> <span data-ttu-id="64505-400">Les exemples incluent des appareils qui utilisent Windows Media DRM pour les périphériques portables, tels qu’un Media Center portable comme iRiver H10, Creative Zen, etc.</span><span class="sxs-lookup"><span data-stu-id="64505-400">Examples include devices that use Windows Media DRM for Portable Devices, such as a Portable Media Center like the iRiver H10, the Creative Zen, and so on.</span></span>
2.  <span data-ttu-id="64505-401">Dans le lecteur Windows Media, cliquez sur l’onglet **synchronisation** .</span><span class="sxs-lookup"><span data-stu-id="64505-401">In Windows Media Player, click the **Sync** tab.</span></span>
3.  <span data-ttu-id="64505-402">Faites glisser le contenu de la bibliothèque vers la zone de **liste synchronisation** sous l’onglet **synchronisation** .</span><span class="sxs-lookup"><span data-stu-id="64505-402">Drag content from the library to the **Sync list** area on the **Sync** tab.</span></span>
4.  <span data-ttu-id="64505-403">Cliquez sur le bouton **Démarrer la synchronisation** .</span><span class="sxs-lookup"><span data-stu-id="64505-403">Click the **Start Sync** button.</span></span>

<span data-ttu-id="64505-404">La capture d’écran suivante montre le suivi 1 dans la zone de **liste synchronisation** et affiche le bouton **Démarrer la synchronisation** dans le lecteur Windows Media 11 :</span><span class="sxs-lookup"><span data-stu-id="64505-404">The following screen shot shows Track 1 in the **Sync list** area and shows the **Start Sync** button in Windows Media Player 11:</span></span>

![capture d’écran montrant comment transférer du contenu dans le lecteur Windows Media 11](images/wmp11-verify-transfer.png)

<span data-ttu-id="64505-406">La capture d’écran suivante montre le suivi 1 dans la zone de **liste synchronisation** et affiche le bouton **Démarrer la synchronisation** dans le lecteur Windows Media 12 :</span><span class="sxs-lookup"><span data-stu-id="64505-406">The following screen shot shows Track 1 in the **Sync list** area and shows the **Start Sync** button in Windows Media Player 12:</span></span>

![capture d’écran montrant comment transférer du contenu dans le lecteur Windows Media 12](images/wmp12-verify-transfer.png)

<span data-ttu-id="64505-408">**Pour vérifier que le contenu acheté peut être transféré vers un autre appareil**</span><span class="sxs-lookup"><span data-stu-id="64505-408">**To verify that purchased content can be transferred to another device**</span></span>

1.  <span data-ttu-id="64505-409">Vérifiez que le contenu acheté est transféré vers l’appareil en lisant le contenu sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="64505-409">Verify that the purchased content is transferred to the device by playing the content on the device.</span></span> <span data-ttu-id="64505-410">Le contenu transféré doit également avoir les métadonnées appropriées.</span><span class="sxs-lookup"><span data-stu-id="64505-410">The transferred content must also have appropriate metadata.</span></span>

2.  <span data-ttu-id="64505-411">Vérifiez que le nombre de synchronisations est décrémenté.</span><span class="sxs-lookup"><span data-stu-id="64505-411">Verify that the sync count is decremented.</span></span>

    <span data-ttu-id="64505-412">Accédez à la bibliothèque et ouvrez les droits d’utilisation du média pour une piste transférée.</span><span class="sxs-lookup"><span data-stu-id="64505-412">Navigate to the library and open the media usage rights for a transferred track.</span></span>

    <span data-ttu-id="64505-413">Si le nombre de fois qu’une piste peut être synchronisée est limité, vérifiez que ce nombre diminue lorsque la piste est transférée.</span><span class="sxs-lookup"><span data-stu-id="64505-413">If the number of times a track can sync is limited, verify that this number decreases when the track is transferred.</span></span>

## <a name="store-features"></a><span data-ttu-id="64505-414">Fonctionnalités du Store</span><span class="sxs-lookup"><span data-stu-id="64505-414">Store Features</span></span>

<span data-ttu-id="64505-415">Les sections suivantes décrivent comment tester diverses fonctionnalités d’un magasin en ligne intégré.</span><span class="sxs-lookup"><span data-stu-id="64505-415">The following sections describe how to test various features of an on-boarded online store.</span></span>

### <a name="managing-an-account"></a><span data-ttu-id="64505-416">Gestion d’un compte</span><span class="sxs-lookup"><span data-stu-id="64505-416">Managing an Account</span></span>

<span data-ttu-id="64505-417">Connectez-vous avec un compte qui a effectué des achats et ouvrez l’historique des achats.</span><span class="sxs-lookup"><span data-stu-id="64505-417">Sign in with an account that has made some purchases and open the purchase history.</span></span>

<span data-ttu-id="64505-418">**Pour vérifier l’historique des achats**</span><span class="sxs-lookup"><span data-stu-id="64505-418">**To verify purchase history**</span></span>

-   <span data-ttu-id="64505-419">Vérifiez que l’historique des achats effectue le suivi des achats précédents.</span><span class="sxs-lookup"><span data-stu-id="64505-419">Verify that the purchase history tracks prior purchases.</span></span>

<span data-ttu-id="64505-420">Si le magasin ou le type de compte prend en charge cette fonctionnalité, tente de restaurer un achat supprimé.</span><span class="sxs-lookup"><span data-stu-id="64505-420">If the store or account type supports this feature, attempt to restore a deleted purchase.</span></span>

<span data-ttu-id="64505-421">**Pour vérifier que les achats précédents peuvent être réacquiss**</span><span class="sxs-lookup"><span data-stu-id="64505-421">**To verify that prior purchases can be reacquired**</span></span>

-   <span data-ttu-id="64505-422">Vérifiez qu’un achat précédent peut être restauré.</span><span class="sxs-lookup"><span data-stu-id="64505-422">Verify that a prior purchase can be restored.</span></span>

<span data-ttu-id="64505-423">Si le magasin prend en charge l’utilisation de plusieurs ordinateurs avec le compte, vérifiez les fonctionnalités offertes par cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="64505-423">If the store supports using multiple computers with the account, verify any functionality that this feature provides.</span></span>

<span data-ttu-id="64505-424">**Pour vérifier la gestion de plusieurs ordinateurs à l’aide d’un seul compte**</span><span class="sxs-lookup"><span data-stu-id="64505-424">**To verify multiple computer management with a single account**</span></span>

-   <span data-ttu-id="64505-425">Vérifiez la fonctionnalité du magasin pour gérer plusieurs ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="64505-425">Verify the store's functionality to manage multiple computers.</span></span>

### <a name="managing-a-store-specific-account"></a><span data-ttu-id="64505-426">Gestion d’un compte Store-Specific</span><span class="sxs-lookup"><span data-stu-id="64505-426">Managing a Store-Specific Account</span></span>

<span data-ttu-id="64505-427">Le magasin peut ne pas avoir de types de compte, de restrictions ou de contenu typiques.</span><span class="sxs-lookup"><span data-stu-id="64505-427">The store might not have typical account types, restrictions, or content.</span></span> <span data-ttu-id="64505-428">Par exemple, un magasin qui loue la vidéo en continu a besoin d’une interface utilisateur pour afficher les loyers actifs et cette interface utilisateur doit être testée.</span><span class="sxs-lookup"><span data-stu-id="64505-428">For example, a store that rents streaming video would need some user interface to display active rentals and that user interface would need to be tested.</span></span>

> [!Note]  
> <span data-ttu-id="64505-429">Bien que Microsoft ne puisse pas certifier les fonctionnalités de compte spécifiques au magasin, pour garantir une expérience utilisateur correcte, vous devez tester cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="64505-429">Although Microsoft cannot certify store-specific account functionality, to ensure a good customer experience, you should test that functionality.</span></span>

 

### <a name="managing-the-info-center"></a><span data-ttu-id="64505-430">Gestion d’info Center</span><span class="sxs-lookup"><span data-stu-id="64505-430">Managing the Info Center</span></span>

<span data-ttu-id="64505-431">Tout d’abord, effectuez les étapes suivantes pour préparer le test de l’État par défaut, puis effectuez l’étape suivante qui suit les étapes initiales pour vérifier que le centre d’informations est désactivé par défaut :</span><span class="sxs-lookup"><span data-stu-id="64505-431">First perform the following steps to prepare for testing the default state, and then perform the next step that follows the initial steps to verify that the Info Center is off by default:</span></span>

1.  <span data-ttu-id="64505-432">Lire du contenu à partir du Store.</span><span class="sxs-lookup"><span data-stu-id="64505-432">Play some content from the store.</span></span>
2.  <span data-ttu-id="64505-433">Basculez en mode de diffusion en cours.</span><span class="sxs-lookup"><span data-stu-id="64505-433">Switch to Now Playing mode.</span></span> <span data-ttu-id="64505-434">Sous Windows XP ou Windows Vista avec le lecteur Windows Media 11, cliquez sur l’onglet **lecture** en cours. Dans Windows 7 avec le lecteur Windows Media 12, cliquez sur le bouton **basculer en cours de lecture** dans le coin inférieur droit.</span><span class="sxs-lookup"><span data-stu-id="64505-434">In Windows XP or Windows Vista with Windows Media Player 11, click the **Now Playing** tab. In Windows 7 with Windows Media Player 12, click the **Switch to Now Playing** button at the lower right corner.</span></span>

<span data-ttu-id="64505-435">**Pour vérifier que le centre d’informations est désactivé par défaut**</span><span class="sxs-lookup"><span data-stu-id="64505-435">**To verify that the Info Center is off by default**</span></span>

-   <span data-ttu-id="64505-436">Vérifiez que le centre d’informations est désactivé par défaut.</span><span class="sxs-lookup"><span data-stu-id="64505-436">Verify that the Info Center is off by default.</span></span>

<span data-ttu-id="64505-437">Si le magasin offre une vue Info Center, lisez du contenu à partir du Store, et Pendant que le contenu est en cours de lecture, passez en mode lecture en cours et activez le centre d’informations.</span><span class="sxs-lookup"><span data-stu-id="64505-437">If the store offers an Info Center view, play some content from the store, and while the content is playing, switch to Now Playing mode and turn Info Center on.</span></span>

<span data-ttu-id="64505-438">Dans Windows XP ou Windows Vista avec le lecteur Windows Media 11, cliquez avec le bouton droit sur la fenêtre de lecture en cours, puis dans le menu contextuel, sélectionnez **affichage du centre d’informations**.</span><span class="sxs-lookup"><span data-stu-id="64505-438">In Windows XP or Windows Vista with Windows Media Player 11, right-click the now-playing window, and then from the context menu select **Info Center View**.</span></span>

<span data-ttu-id="64505-439">La capture d’écran suivante montre le menu contextuel dans le lecteur Windows Media 11 :</span><span class="sxs-lookup"><span data-stu-id="64505-439">The following screen shot shows the context menu in Windows Media Player 11:</span></span>

![capture d’écran montrant comment accéder au centre d’informations d’un magasin dans le lecteur Windows Media 11](images/wmp11-info-center.png)

<span data-ttu-id="64505-441">Dans Windows 7 avec le lecteur Windows Media 12, cliquez avec le bouton droit sur la fenêtre de lecture maintenant, dans le menu contextuel, sélectionnez **visualisations**, puis cliquez sur **affichage Centre d’informations**.</span><span class="sxs-lookup"><span data-stu-id="64505-441">In Windows 7 with Windows Media Player 12, right-click the now-playing window, on the context menu select **Visualizations**, and then click **Info Center View**.</span></span>

<span data-ttu-id="64505-442">La capture d’écran suivante montre le menu contextuel dans le lecteur Windows Media 12 :</span><span class="sxs-lookup"><span data-stu-id="64505-442">The following screen shot shows the context menu in Windows Media Player 12:</span></span>

![capture d’écran montrant comment accéder au centre d’informations d’un magasin dans le lecteur Windows Media 12](images/wmp12-info-center.png)

<span data-ttu-id="64505-444">**Pour vérifier que le centre d’informations est fonctionnel**</span><span class="sxs-lookup"><span data-stu-id="64505-444">**To verify that the Info Center is functional**</span></span>

-   <span data-ttu-id="64505-445">Vérifiez que le centre d’informations affiche des informations sur le média dans la zone de diffusion en cours.</span><span class="sxs-lookup"><span data-stu-id="64505-445">Verify that the Info Center shows media information in the now-playing area.</span></span> <span data-ttu-id="64505-446">La capture d’écran suivante montre un exemple d’informations de ce type de média :</span><span class="sxs-lookup"><span data-stu-id="64505-446">The following screen shot shows an example of such media information:</span></span>

    ![capture d’écran montrant les fonctionnalités du centre d’informations d’un magasin](images/media-information.png)

<span data-ttu-id="64505-448">Si des liens d’achat ou d’autres liens apparaissent sur la page, cliquez sur les liens.</span><span class="sxs-lookup"><span data-stu-id="64505-448">If any buy links or other links appear on the page, click the links.</span></span>

<span data-ttu-id="64505-449">**Pour vérifier les liens dans la vue Centre d’informations**</span><span class="sxs-lookup"><span data-stu-id="64505-449">**To verify links in the Info Center view**</span></span>

-   <span data-ttu-id="64505-450">Vérifiez que les liens affichent le magasin.</span><span class="sxs-lookup"><span data-stu-id="64505-450">Verify that the links show the store.</span></span>

    <span data-ttu-id="64505-451">Le lecteur Windows Media doit basculer vers le magasin dans sa bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="64505-451">The Windows Media Player should switch to the store in its library.</span></span>

## <a name="store-interaction"></a><span data-ttu-id="64505-452">Interaction du Store</span><span class="sxs-lookup"><span data-stu-id="64505-452">Store Interaction</span></span>

<span data-ttu-id="64505-453">Les sections suivantes décrivent comment tester l’interaction entre les autres magasins et le magasin que vous testez.</span><span class="sxs-lookup"><span data-stu-id="64505-453">The following sections describe how to test interaction between the other stores and the store that you are testing.</span></span>

### <a name="yielding-to-the-active-store"></a><span data-ttu-id="64505-454">Donner au magasin actif</span><span class="sxs-lookup"><span data-stu-id="64505-454">Yielding to the Active Store</span></span>

<span data-ttu-id="64505-455">Basculez vers un magasin autre que le magasin en cours de test.</span><span class="sxs-lookup"><span data-stu-id="64505-455">Switch to a store other than the store being tested.</span></span>

<span data-ttu-id="64505-456">**Pour vérifier le rendement du magasin actif**</span><span class="sxs-lookup"><span data-stu-id="64505-456">**To verify yielding to the active store**</span></span>

-   <span data-ttu-id="64505-457">Vérifiez que le magasin testé produit le magasin actif.</span><span class="sxs-lookup"><span data-stu-id="64505-457">Verify that the tested store yields to the active store.</span></span>

### <a name="preventing-the-tested-store-from-taking-over-the-active-store"></a><span data-ttu-id="64505-458">Empêcher le magasin testé de prendre le contrôle du magasin actif</span><span class="sxs-lookup"><span data-stu-id="64505-458">Preventing the Tested Store From Taking Over the Active Store</span></span>

-   <span data-ttu-id="64505-459">Avec un autre magasin sélectionné, fermez le lecteur Windows Media, puis redémarrez l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="64505-459">With another store selected, close Windows Media Player and restart the computer.</span></span>
-   <span data-ttu-id="64505-460">Lancez le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="64505-460">Launch Windows Media Player.</span></span>

<span data-ttu-id="64505-461">**Pour vérifier que le magasin testé ne prend pas le contrôle**</span><span class="sxs-lookup"><span data-stu-id="64505-461">**To verify that the tested store does not take over**</span></span>

-   <span data-ttu-id="64505-462">Vérifiez que le magasin actif le plus récent s’affiche et que le magasin testé n’apparaît pas.</span><span class="sxs-lookup"><span data-stu-id="64505-462">Verify that the most recently active store appears and that the tested store does not appear.</span></span>

### <a name="accessing-a-store-in-high-contrast-mode"></a><span data-ttu-id="64505-463">Accès à un magasin en mode High-Contrast</span><span class="sxs-lookup"><span data-stu-id="64505-463">Accessing a Store in High-Contrast Mode</span></span>

<span data-ttu-id="64505-464">Commencez par activer le mode de contraste élevé en appuyant sur MAJ gauche + ALT gauche + Impr. écran, puis procédez comme suit pour vérifier l’accessibilité à contraste élevé :</span><span class="sxs-lookup"><span data-stu-id="64505-464">First enable high-contrast mode by pressing LEFT SHIFT+LEFT ALT+PRINT SCREEN, and then perform the following steps to verify high-contrast accessibility:</span></span>

<span data-ttu-id="64505-465">**Pour vérifier que le magasin est accessible en mode de contraste élevé**</span><span class="sxs-lookup"><span data-stu-id="64505-465">**To verify that the store is accessible in high-contrast mode**</span></span>

1.  <span data-ttu-id="64505-466">Vérifiez que l’interface utilisateur de connexion est intacte et fonctionnelle.</span><span class="sxs-lookup"><span data-stu-id="64505-466">Verify that the log-in user interface is intact and functional.</span></span>
2.  <span data-ttu-id="64505-467">Vérifiez que toutes les fenêtres et boîtes de dialogue s’affichent correctement.</span><span class="sxs-lookup"><span data-stu-id="64505-467">Verify that all windows and dialog boxes appear correctly.</span></span>
3.  <span data-ttu-id="64505-468">Acheter un support.</span><span class="sxs-lookup"><span data-stu-id="64505-468">Purchase media.</span></span> <span data-ttu-id="64505-469">Vérifiez que les boutons achat et téléchargement, les gestionnaires de téléchargement, les informations sur les prix, etc. sont visibles.</span><span class="sxs-lookup"><span data-stu-id="64505-469">Verify that purchase and download buttons, download managers, price information, and so on is visible.</span></span>
4.  <span data-ttu-id="64505-470">Vérifiez que vous pouvez diffuser, graver et synchroniser.</span><span class="sxs-lookup"><span data-stu-id="64505-470">Verify that you can stream, burn, and synchronize.</span></span>
5.  <span data-ttu-id="64505-471">Recherchez du texte tronqué et des éléments d’interface utilisateur, du texte qui n’est pas lisible et d’autres défauts visibles.</span><span class="sxs-lookup"><span data-stu-id="64505-471">Look for clipped text and user-interface elements, text that is not legible, and other visible defects.</span></span>

### <a name="securing-a-store"></a><span data-ttu-id="64505-472">Sécurisation d’un magasin</span><span class="sxs-lookup"><span data-stu-id="64505-472">Securing a Store</span></span>

<span data-ttu-id="64505-473">Pour vérifier la sécurité du compte, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="64505-473">Perform the following steps to verify account security:</span></span>

<span data-ttu-id="64505-474">**Pour vérifier la sécurité du compte**</span><span class="sxs-lookup"><span data-stu-id="64505-474">**To verify account security**</span></span>

1.  <span data-ttu-id="64505-475">Entrez les informations de compte incorrectes dans la page de connexion et la boîte de dialogue et vérifiez que le magasin les rejette.</span><span class="sxs-lookup"><span data-stu-id="64505-475">Enter malformed account information into the log-in page and dialog box and verify that the store rejects it.</span></span>
2.  <span data-ttu-id="64505-476">Connectez-vous, affichez la page du compte, puis déconnectez-vous.</span><span class="sxs-lookup"><span data-stu-id="64505-476">Sign in, view the account page, and sign out.</span></span>
3.  <span data-ttu-id="64505-477">Cliquez sur le bouton précédent dans le lecteur Windows Media et vérifiez que vous ne voyez pas les informations de compte d’utilisateur précédentes.</span><span class="sxs-lookup"><span data-stu-id="64505-477">Click the back button in Windows Media Player, and verify that you do not see the previous user account information.</span></span>

 

 




