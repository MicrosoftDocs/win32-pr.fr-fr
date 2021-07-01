---
title: 'Cas de test des jeux pour Windows : bonnes pratiques pour les jeux sur Windows XP, Windows Vista, Windows 7 et Windows 8'
description: Cet article fournit des cas de test pour les jeux pour Windows.
ms.assetid: bbe84d3f-e7ff-f14f-ec25-ae1c980749fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b13a4934c539579e49c9b00c60f3603bd64c711
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120274"
---
# <a name="games-for-windows-test-cases-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8"></a><span data-ttu-id="1c8dd-103">Jeux pour les cas de test Windows : meilleures pratiques pour les jeux sur Windows XP, Windows Vista, Windows 7 et Windows 8</span><span class="sxs-lookup"><span data-stu-id="1c8dd-103">Games for Windows Test Cases: Best Practices for Games on Windows XP, Windows Vista, Windows 7, and Windows 8</span></span>

<span data-ttu-id="1c8dd-104">Cet article fournit des cas de test pour les jeux pour Windows.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-104">This article provides test cases for games for Windows.</span></span>

## <a name="how-to-use-this-article"></a><span data-ttu-id="1c8dd-105">Procédure d'utilisation de cet article</span><span class="sxs-lookup"><span data-stu-id="1c8dd-105">How to Use This Article</span></span>

<span data-ttu-id="1c8dd-106">Cet article comporte trois sections principales :</span><span class="sxs-lookup"><span data-stu-id="1c8dd-106">There are three main sections to this article:</span></span>

<dl> <dt>

<span data-ttu-id="1c8dd-107"><span id="Test_Requirements"></span><span id="test_requirements"></span><span id="TEST_REQUIREMENTS"></span>**Spécifications de test**</span><span class="sxs-lookup"><span data-stu-id="1c8dd-107"><span id="Test_Requirements"></span><span id="test_requirements"></span><span id="TEST_REQUIREMENTS"></span>**Test Requirements**</span></span>
</dt> <dd>

<span data-ttu-id="1c8dd-108">Chaque spécification de test dans ce document comporte quatre sections principales : un titre et une table avec trois sections notables (colonne de gauche, droite en haut, à droite en bas).</span><span class="sxs-lookup"><span data-stu-id="1c8dd-108">Each test requirement in this document has four main sections: a title and a table with three notable sections (left column, right top, right bottom).</span></span>

<dl> <dt>

<span data-ttu-id="1c8dd-109"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>Bonhomme</span><span class="sxs-lookup"><span data-stu-id="1c8dd-109"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>Title</span></span>
</dt> <dd>

<span data-ttu-id="1c8dd-110">Nom du cas de test.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-110">Name of the test case.</span></span>

</dd> <dt>

<span data-ttu-id="1c8dd-111"><span id="Box__far_left_column"></span><span id="box__far_left_column"></span><span id="BOX__FAR_LEFT_COLUMN"></span>Box, colonne de gauche</span><span class="sxs-lookup"><span data-stu-id="1c8dd-111"><span id="Box__far_left_column"></span><span id="box__far_left_column"></span><span id="BOX__FAR_LEFT_COLUMN"></span>Box, far left column</span></span>
</dt> <dd>

<span data-ttu-id="1c8dd-112">Noms des systèmes d’exploitation auxquels s’applique le cas de test.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-112">Names of the operating systems to which the test case applies.</span></span>

</dd> <dt>

<span data-ttu-id="1c8dd-113"><span id="Box__right_top"></span><span id="box__right_top"></span><span id="BOX__RIGHT_TOP"></span>Box, à droite en haut</span><span class="sxs-lookup"><span data-stu-id="1c8dd-113"><span id="Box__right_top"></span><span id="box__right_top"></span><span id="BOX__RIGHT_TOP"></span>Box, right top</span></span>
</dt> <dd>

<span data-ttu-id="1c8dd-114">Bref résumé du cas de test.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-114">Brief summary of the test case.</span></span>

</dd> <dt>

<span data-ttu-id="1c8dd-115"><span id="Box__right_bottom"></span><span id="box__right_bottom"></span><span id="BOX__RIGHT_BOTTOM"></span>Box, à droite en bas</span><span class="sxs-lookup"><span data-stu-id="1c8dd-115"><span id="Box__right_bottom"></span><span id="box__right_bottom"></span><span id="BOX__RIGHT_BOTTOM"></span>Box, right bottom</span></span>
</dt> <dd>

<span data-ttu-id="1c8dd-116">Détails du cas de test réel.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-116">Details of the actual test case.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="1c8dd-117"><span id="Sample_Test_Script"></span><span id="sample_test_script"></span><span id="SAMPLE_TEST_SCRIPT"></span>**Exemple de script de test**</span><span class="sxs-lookup"><span data-stu-id="1c8dd-117"><span id="Sample_Test_Script"></span><span id="sample_test_script"></span><span id="SAMPLE_TEST_SCRIPT"></span>**Sample Test Script**</span></span>
</dt> <dd>

<span data-ttu-id="1c8dd-118">Cette section est un exemple de la séquence qu’une passe de test typique suivra si vous utilisez les spécifications de test comme guide.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-118">This section is a sample of the sequence that a typical test pass would follow if using the test requirements as a guide.</span></span>

</dd> <dt>

<span data-ttu-id="1c8dd-119"><span id="Test_Tool_Notes"></span><span id="test_tool_notes"></span><span id="TEST_TOOL_NOTES"></span>**Notes de l’outil de test**</span><span class="sxs-lookup"><span data-stu-id="1c8dd-119"><span id="Test_Tool_Notes"></span><span id="test_tool_notes"></span><span id="TEST_TOOL_NOTES"></span>**Test Tool Notes**</span></span>
</dt> <dd>

<span data-ttu-id="1c8dd-120">Cette section contient des remarques détaillées sur chacun des outils de test utilisés pour vérifier les conditions de réussite ou d’échec dans les spécifications de test.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-120">This section contains detailed notes on each of the test tools used to verify pass or fail conditions in the test requirements.</span></span>

</dd> </dl>

## <a name="test-requirements"></a><span data-ttu-id="1c8dd-121">Spécifications de test</span><span class="sxs-lookup"><span data-stu-id="1c8dd-121">Test Requirements</span></span>

### <a name="1-game-requirements"></a><span data-ttu-id="1c8dd-122">1. spécifications du jeu</span><span class="sxs-lookup"><span data-stu-id="1c8dd-122">1. Game Requirements</span></span>

### <a name="11-windows-games-explorer"></a><span data-ttu-id="1c8dd-123">Explorateur de jeux Windows 1,1</span><span class="sxs-lookup"><span data-stu-id="1c8dd-123">1.1 Windows Games Explorer</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c8dd-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c8dd-124">Windows 7</span></span><br/> <span data-ttu-id="1c8dd-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c8dd-125">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="1c8dd-126">Le jeu doit être visible dans l’Explorateur de jeux sur Windows Vista et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-126">The game must be visible within the Games Explorer on Windows Vista and Windows 7.</span></span> <span data-ttu-id="1c8dd-127">Lorsque cette option est sélectionnée, le jeu doit également afficher les métadonnées correctes.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-127">When selected, the game must also display correct metadata.</span></span> <span data-ttu-id="1c8dd-128">L’installation ne doit pas créer de raccourci pour lancer le jeu sur le bureau, dans le menu Démarrer ou dans un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-128">The installation must not create a shortcut to launch the game on the desktop, in the Start menu, or in any other location.</span></span> <span data-ttu-id="1c8dd-129">Les tâches et les raccourcis de suppression ne doivent pas être créés.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-129">Tasks and shortcuts for removal must not be created.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="1c8dd-130">Après avoir installé le jeu, ouvrez l’Explorateur de jeux.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-130">After installing the game, open Games Explorer.</span></span></li>
<li><span data-ttu-id="1c8dd-131">Vérifiez que l’icône de jeu s’affiche dans l’Explorateur de jeux.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-131">Verify that the game icon displays in Games Explorer.</span></span></li>
<li><span data-ttu-id="1c8dd-132">Cliquez avec le bouton droit sur l’icône et testez chaque tâche de support de lecture & définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-132">Right-click the icon and test each application-defined play & support task.</span></span></li>
<li><span data-ttu-id="1c8dd-133">Cliquez sur l’icône et vérifiez que les métadonnées (éditeur, développeur, genre, date de publication, version) s’affichent en bas et sont correctes.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-133">Click the icon and verify that the metadata (publisher, developer, genre, release date, version) at the bottom displays and is correct.</span></span></li>
<li><span data-ttu-id="1c8dd-134">Vérifiez que l’icône du jeu affiche des informations sur l’indice de performance Windows (WEI) dans l’Explorateur de jeux.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-134">Verify that the game icon displays Windows Experience Index (WEI) information in Games Explorer.</span></span></li>
<li><span data-ttu-id="1c8dd-135">Vérifiez que les liens hypertexte de jeu pour les métadonnées fonctionnent correctement dans l’Explorateur de jeux.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-135">Verify that game hyperlinks for metadata work correctly in Games Explorer.</span></span> <span data-ttu-id="1c8dd-136">(Si les liens hypertexte ne s’affichent pas, il s’agit d’un signe possible que l’exe n’est pas signé ; consultez la <a href="#23-sign-files">section 2,3</a>.)</span><span class="sxs-lookup"><span data-stu-id="1c8dd-136">(If hyperlinks don't show up, then this is a possible sign that the exe isn't signed; see <a href="#23-sign-files">section 2.3</a>.)</span></span></li>
<li><span data-ttu-id="1c8dd-137">Vérifiez que le jeu affiche une évaluation précise du contrôle parental dans l’Explorateur de jeux.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-137">Verify that the game displays accurate parental control rating in Games Explorer.</span></span> <span data-ttu-id="1c8dd-138">(S’il indique non évalué, vérifiez qu’il s’agit d’un jeu non classé ; sinon, il s’agit d’un indicateur que l’exe n’est pas signé ; consultez la <a href="#23-sign-files">section 2,3</a>.)</span><span class="sxs-lookup"><span data-stu-id="1c8dd-138">(If it says unrated, then verify that this is an unrated game; otherwise, this is an indicator that the exe isn't signed; see <a href="#23-sign-files">section 2.3</a>.)</span></span></li>
<li><span data-ttu-id="1c8dd-139">Vérifiez que le jeu ne place pas de raccourcis de lancement sur le Bureau de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-139">Verify that the game does not place launch shortcuts on user desktop.</span></span></li>
<li><span data-ttu-id="1c8dd-140">Cliquez sur Démarrer-> tous les programmes.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-140">Click Start -> All Programs.</span></span></li>
<li><span data-ttu-id="1c8dd-141">Vérifiez que le jeu ne place pas de raccourcis de lancement dans le menu Démarrer.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-141">Verify that the game does not place launch shortcuts in the Start Menu.</span></span></li>
<li><span data-ttu-id="1c8dd-142">Vérifiez que le jeu ne place pas les raccourcis de désinstallation dans le menu démarrer en dehors du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-142">Verify that the game does not place uninstall shortcuts in Start Menu outside of Control Panel.</span></span></li>
<li><span data-ttu-id="1c8dd-143">Si le jeu est distribué numériquement, vérifiez que le fournisseur de services s’affiche dans l’Explorateur Windows Games.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-143">If the game is distributed digitally, verify that the service provider appears in Windows Games Explorer.</span></span></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="12-windows-family-safety--parental-controls"></a><span data-ttu-id="1c8dd-144">Contrôle parental/sécurité de la famille Windows 1,2</span><span class="sxs-lookup"><span data-stu-id="1c8dd-144">1.2 Windows Family Safety / Parental Controls</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c8dd-145">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c8dd-145">Windows 7</span></span><br/> <span data-ttu-id="1c8dd-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c8dd-146">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="1c8dd-147">Le jeu doit s’exécuter dans le contexte d’un &quot; utilisateur standard &quot; .</span><span class="sxs-lookup"><span data-stu-id="1c8dd-147">Game must execute within the context of a &quot;Standard User&quot;.</span></span> <span data-ttu-id="1c8dd-148">Le contrôle parental doit pouvoir bloquer le jeu.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-148">Parental Controls must be able to block the game.</span></span> <span data-ttu-id="1c8dd-149">Vérifiez que le fichier GDF contient des noms EXE.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-149">Verify that the GDF has EXE names.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="1c8dd-150">Créez un compte d’utilisateur standard dans Windows Vista ou Windows 7 appelé Toby.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-150">Create a Standard User account in Windows Vista or Windows 7 called Toby.</span></span> <span data-ttu-id="1c8dd-151">Démarrer-> le panneau de configuration-> ajouter ou supprimer des comptes d’utilisateur-> créer un nouveau compte</span><span class="sxs-lookup"><span data-stu-id="1c8dd-151">Start -> Control Panel -> Add or Remove User Accounts -> Create New Account</span></span></li>
<li><span data-ttu-id="1c8dd-152">En tant que Jane, à partir du compte administrateur, configurez les contrôles parentaux pour le jeu.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-152">As Jane, from Administrator account set up Parental Controls for the game.</span></span> <span data-ttu-id="1c8dd-153">Démarrer-> panneau de configuration-> configurer des contrôles parentaux pour les Toby d’un utilisateur ></span><span class="sxs-lookup"><span data-stu-id="1c8dd-153">Start -> Control Panel -> Set Up Parental Controls for Any User -> Toby</span></span>
<ol>
<li><span data-ttu-id="1c8dd-154">Vérifiez que le jeu est lancé à partir de l’icône Explorateur de jeux.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-154">Verify that the game launches from the Games Explorer icon.</span></span></li>
<li><span data-ttu-id="1c8dd-155">Vérifiez que le jeu affiche une évaluation exacte du contrôle parental sous le titre du jeu dans le panneau de configuration du contrôle parental.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-155">Verify that the game displays accurate Parental Control Rating below the game title in the Parental Controls Control Panel.</span></span></li>
<li><span data-ttu-id="1c8dd-156">Avant d’appliquer les contrôles parentaux, vérifiez que le jeu ne demande pas d’informations d’identification d’administrateur au lancement.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-156">Before applying Parental Controls, verify that the game does not prompt for Administrator Credentials on launch.</span></span></li>
<li><span data-ttu-id="1c8dd-157">Définissez contrôle parental &quot; sur activé &quot; .</span><span class="sxs-lookup"><span data-stu-id="1c8dd-157">Set Parental Controls to &quot;On&quot;.</span></span></li>
<li><span data-ttu-id="1c8dd-158">Dans la section Paramètres Windows, cliquez sur jeux.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-158">In the Windows Settings section, click Games.</span></span></li>
<li><span data-ttu-id="1c8dd-159">Cliquez sur OK (le paramètre doit maintenant être &quot; AO/All Games &quot; ).</span><span class="sxs-lookup"><span data-stu-id="1c8dd-159">Click OK (setting should now be &quot;AO / all games&quot;).</span></span></li>
<li><span data-ttu-id="1c8dd-160">Vérifiez que le jeu s’exécute avec ces paramètres en tant qu’utilisateur Jane.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-160">Verify that the game runs with these settings as User Jane.</span></span></li>
<li><span data-ttu-id="1c8dd-161">Déconnectez-vous en tant que Jane et connectez-vous en tant que Toby.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-161">Log off as Jane and log on as Toby.</span></span></li>
<li><span data-ttu-id="1c8dd-162">Vérifiez que le jeu s’exécute avec ces paramètres en tant qu’utilisateur Toby.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-162">Verify that the game runs with these settings as User Toby.</span></span></li>
<li><span data-ttu-id="1c8dd-163">Déconnectez-vous en tant que Toby et connectez-vous en tant que Jane.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-163">Log off as Toby and log on as Jane.</span></span></li>
<li><span data-ttu-id="1c8dd-164">Revenez à l’écran précédent et sélectionnez &quot; définir les évaluations de jeux &quot; .</span><span class="sxs-lookup"><span data-stu-id="1c8dd-164">Go back to the previous screen and select &quot;Set Game Ratings&quot;.</span></span></li>
<li><p><span data-ttu-id="1c8dd-165">Sélectionnez une évaluation inférieure à l’évaluation de la ESRB du jeu.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-165">Select a rating lower than the game's ESRB Rating.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="1c8dd-166">Si le jeu n’est pas évalué, ignorez cette étape et passez à la partie suivante de ce test.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-166">If the game is not rated, then skip this step and move onto the next part of this test.</span></span> <span data-ttu-id="1c8dd-167">Il peut être nécessaire de choisir un système d’évaluation différent pour trouver une évaluation du jeu, en fonction des paramètres régionaux de langue de la référence SKU testée.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-167">It may be necessary to choose a different rating system to find a game rating, depending on the language locale of the SKU being tested.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="1c8dd-168">Déconnectez-vous en tant que Jane et connectez-vous en tant que Toby.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-168">Log off as Jane and log on as Toby.</span></span></li>
<li><span data-ttu-id="1c8dd-169">Vérifiez que le jeu n’est pas lancé pour l’utilisateur Toby lorsque ESRB est bloqué par l’utilisateur Jane.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-169">Verify that the game does not launch for User Toby when ESRB is blocked by User Jane.</span></span></li>
<li><span data-ttu-id="1c8dd-170">Déconnectez-vous en tant que Toby et connectez-vous en tant que Jane.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-170">Log off as Toby and log on as Jane.</span></span></li>
<li><span data-ttu-id="1c8dd-171">En cas de modification précédente, restaurez les paramètres ESRB.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-171">If changed previously, restore the ESRB settings.</span></span></li>
<li><span data-ttu-id="1c8dd-172">S’il n’existe aucun paramètre ESRB, sélectionnez &quot; bloquer ou autoriser des jeux spécifiques, &quot; puis sélectionnez le jeu par son nom.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-172">If there are no ESRB settings, then select &quot;Block or Allow Specific Games&quot; and select the game by name.</span></span></li>
<li><span data-ttu-id="1c8dd-173">Déconnectez-vous en tant que Jane et connectez-vous en tant que Toby.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-173">Log off as Jane and log on as Toby.</span></span></li>
<li><span data-ttu-id="1c8dd-174">Vérifiez que le jeu n’est pas lancé pour l’utilisateur Toby lorsque l’utilisateur ou le nom est bloqué par l’utilisateur Jane.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-174">Verify that the game does not launch for User Toby when EXE/Name is blocked by User Jane.</span></span></li>
<li><span data-ttu-id="1c8dd-175">Déconnectez-vous en tant que Toby et revenez sous le titre Jane.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-175">Log off as Toby and back on as Jane.</span></span></li>
<li><span data-ttu-id="1c8dd-176">Pour Jane, ouvrez contrôles utilisateur-> restrictions d’application.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-176">As Jane, open User Controls -> Application Restrictions.</span></span></li>
<li><span data-ttu-id="1c8dd-177">Cliquez sur &quot; Toby ne peut utiliser que les programmes que j’autorise &quot; , puis cliquez sur OK (autrement dit, n’autoriser aucun exe).</span><span class="sxs-lookup"><span data-stu-id="1c8dd-177">Click &quot;Toby can only use the programs I allow&quot; and click OK (that is, allow no exes).</span></span></li>
<li><span data-ttu-id="1c8dd-178">Accéder aux contrôles utilisateur | Les jeux contrôlent et permettent le jeu spécifique à l’aide de l’évaluation ESRB.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-178">Go to User Controls | Games Controls and allow the specific game using the ESRB rating.</span></span></li>
<li><span data-ttu-id="1c8dd-179">Déconnectez-vous en tant que Jane et connectez-vous en tant que Toby et essayez de jouer au jeu.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-179">Log off as Jane, and log on as Toby and try to play the game.</span></span></li>
<li><span data-ttu-id="1c8dd-180">Vérifiez que le jeu n’est pas bloqué et que Toby peut le lire quand &quot; aucun exe &quot; n’est défini.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-180">Verify that the game is NOT blocked and that Toby can play it when &quot;allow no exes&quot; is set.</span></span></li>
</ol></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="13-windows-vista-rich-saved-games"></a><span data-ttu-id="1c8dd-181">1,3 jeux enrichis Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c8dd-181">1.3 Windows Vista Rich Saved Games</span></span>

<span data-ttu-id="1c8dd-182">Cette exigence a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-182">This requirement has been retired.</span></span>

### <a name="14-xbox-360-common-controller-for-windows-conditional-requirement"></a><span data-ttu-id="1c8dd-183">1,4 Xbox 360 contrôleur commun pour Windows \[ condition conditionnelle\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-183">1.4 Xbox 360 Common Controller for Windows \[Conditional Requirement\]</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c8dd-184">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c8dd-184">Windows 7</span></span><br/> <span data-ttu-id="1c8dd-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c8dd-185">Windows Vista</span></span><br/> <span data-ttu-id="1c8dd-186">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1c8dd-186">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1c8dd-187">Les jeux qui prennent en charge les contrôleurs de manette doivent prendre en charge le contrôleur Xbox 360 pour Windows à l’aide de l’API XInput.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-187">Games that support gamepad controllers must support the Xbox 360 Controller for Windows using the XInput API.</span></span> <span data-ttu-id="1c8dd-188">Toutes les références aux déclencheurs et aux boutons du contrôleur commun doivent utiliser les noms Xbox 360.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-188">All references to common controller triggers and buttons must use the Xbox 360 names.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="1c8dd-189">Lancez le jeu.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-189">Launch the game.</span></span></li>
<li><span data-ttu-id="1c8dd-190">Accédez aux options du contrôleur.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-190">Go into the controller options.</span></span> **</li>
<li><span data-ttu-id="1c8dd-191">Vérifiez que le jeu reconnaît le contrôleur Xbox 360 pour Windows comme périphérique d’entrée.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-191">Verify that the game recognizes Xbox 360 Controller for Windows as an input device.</span></span></li>
<li><span data-ttu-id="1c8dd-192">Jouez au jeu et vérifiez que le jeu et le système de menus sont contrôlable avec le contrôleur Xbox 360 pour Windows.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-192">Play the game and verify that the game and menu system are controllable with Xbox 360 Controller for Windows.</span></span></li>
<li><span data-ttu-id="1c8dd-193">Vérifiez que le contrôleur Xbox 360 pour Windows se comporte conformément aux normes acceptées.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-193">Verify that the Xbox 360 Controller for Windows behaves according to accepted standards.</span></span> <span data-ttu-id="1c8dd-194">(B pour précédent, A pour accepter, démarrer pour dans le menu jeu/suspendre ou accepter, etc.)</span><span class="sxs-lookup"><span data-stu-id="1c8dd-194">(B for back, A for accept, Start for in game menu/pause or accept, etc.)</span></span></li>
<li><span data-ttu-id="1c8dd-195">Vérifiez que le jeu fait référence aux boutons et aux déclencheurs de contrôleur à l’aide des noms Xbox 360.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-195">Verify that the game refers to the controller buttons and triggers using Xbox 360 names.</span></span></li>
</ol>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1c8dd-196">Si le jeu ne prend pas en charge un contrôleur de jeu et/ou ne prend en charge que le clavier/la souris, ignorez ce cas de test.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-196">If the game does not support a game controller and/or only supports keyboard/mouse, then skip this test case.</span></span>
</blockquote>
<br/> <span data-ttu-id="1c8dd-197">\* \* Les paramètres du contrôleur sont peut-être situés en dehors du jeu.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-197">\*\* Settings for the controller might be located outside of the game.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="15-multiple-aspect-ratios-and-resolutions"></a><span data-ttu-id="1c8dd-198">1,5 plusieurs proportions et résolutions</span><span class="sxs-lookup"><span data-stu-id="1c8dd-198">1.5 Multiple Aspect Ratios and Resolutions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c8dd-199">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c8dd-199">Windows 7</span></span><br/> <span data-ttu-id="1c8dd-200">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c8dd-200">Windows Vista</span></span><br/> <span data-ttu-id="1c8dd-201">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1c8dd-201">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1c8dd-202">Le jeu doit prendre en charge au moins les proportions et les résolutions d’écran associées suivantes :</span><span class="sxs-lookup"><span data-stu-id="1c8dd-202">The game must support at least the following aspect ratios and associated screen resolutions:</span></span> <br/>
<ul>
<li><span data-ttu-id="1c8dd-203">4:3 &quot; normal &quot; (800 600 ou 1024 768)</span><span class="sxs-lookup"><span data-stu-id="1c8dd-203">4:3 &quot;normal&quot; (800 600 or 1024 768)</span></span></li>
<li><span data-ttu-id="1c8dd-204">&quot;écran large 16:9 &quot; (1280 720)</span><span class="sxs-lookup"><span data-stu-id="1c8dd-204">16:9 &quot;widescreen&quot; (1280 720)</span></span></li>
<li><span data-ttu-id="1c8dd-205">16:10 &quot; grand écran &quot; (1152 720, 1680 1050 ou 800 480)</span><span class="sxs-lookup"><span data-stu-id="1c8dd-205">16:10 &quot;widescreen&quot; (1152 720, 1680 1050, or 800 480)</span></span></li>
</ul></td>
</tr>
<tr class="even">

<td><span data-ttu-id="1c8dd-206">Recherchez les options vidéo pour le jeu (cela peut être dans notre jeu).</span><span class="sxs-lookup"><span data-stu-id="1c8dd-206">Locate the Video Options for the game (this may be in our out of game).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1c8dd-207">Les tests suivants doivent être effectués sur une analyse panoramique.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-207">The following tests must be done on a widescreen monitor.</span></span>
</blockquote>
<br/>
<ol>
<li><span data-ttu-id="1c8dd-208">Dans la section résolution vidéo, sélectionnez 800 600 ou 1024 768.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-208">In the video resolution section, select 800 600 or 1024 768.</span></span></li>
<li><span data-ttu-id="1c8dd-209">Vérifiez que le jeu s’exécute avec une résolution de proportions de 4:3.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-209">Verify that the game runs at a 4:3 Aspect Ratio resolution.</span></span></li>
<li><span data-ttu-id="1c8dd-210">Dans la section résolution vidéo, sélectionnez 1280 720.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-210">In the video resolution section, select 1280 720.</span></span></li>
<li><span data-ttu-id="1c8dd-211">Vérifiez que le jeu s’exécute avec une résolution de proportions de 16:9.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-211">Verify that the game runs at a 16:9 Aspect Ratio resolution.</span></span></li>
<li><span data-ttu-id="1c8dd-212">Dans la section résolution vidéo, sélectionnez 1680 1050, 800 480 ou 1152 720.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-212">In the video resolution section, select 1680 1050, 800 480, or 1152 720.</span></span></li>
<li><span data-ttu-id="1c8dd-213">Vérifiez que le jeu s’exécute avec une résolution de proportions de 16:10.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-213">Verify that the game runs at a 16:10 Aspect Ratio resolution.</span></span></li>
<li><span data-ttu-id="1c8dd-214">Vérifiez que le jeu n’étire pas l’image et, à son tour, présente une zone de vue plus vaste.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-214">Verify that the game does not stretch the picture and in turn presents a wider area of view.</span></span></li>
<li><span data-ttu-id="1c8dd-215">Vérifiez que le jeu demande à l’utilisateur quand une modification est apportée à la résolution.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-215">Verify that the game prompts the user when a change is made to the resolution.</span></span></li>
<li><span data-ttu-id="1c8dd-216">Si l’utilisateur n’accepte pas dans les 15 secondes, vérifiez que l’affichage est rétabli sur le paramètre précédent.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-216">If the user does not accept within 15 seconds, verify that the display reverts to the previous setting.</span></span></li>
<li><span data-ttu-id="1c8dd-217">Vérifiez que le jeu n’ajoute pas de barres noires à gauche et à droite de la zone de jeu.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-217">Verify that the game does not add black bars to the left and right of the game play area.</span></span> <span data-ttu-id="1c8dd-218">(Dans ce cas, la zone de jeu se trouve toujours dans un ratio 4:3 au milieu de l’écran.)</span><span class="sxs-lookup"><span data-stu-id="1c8dd-218">(In this case, you will see the game area still in a 4:3 ratio in the middle of the screen.)</span></span></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="16-windows-media-center"></a><span data-ttu-id="1c8dd-219">1,6 Windows Media Center</span><span class="sxs-lookup"><span data-stu-id="1c8dd-219">1.6 Windows Media Center</span></span>

<span data-ttu-id="1c8dd-220">Cette exigence a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-220">This requirement has been retired.</span></span>

### <a name="17-direct3d-conditional-requirement"></a><span data-ttu-id="1c8dd-221">1,7 \[ condition conditionnelle Direct3D\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-221">1.7 Direct3D \[Conditional Requirement\]</span></span>



| <span data-ttu-id="1c8dd-222">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="1c8dd-222">OS</span></span>                                                                    | <span data-ttu-id="1c8dd-223">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c8dd-223">Requirement</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c8dd-224">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c8dd-224">Windows 7</span></span><br/> <span data-ttu-id="1c8dd-225">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c8dd-225">Windows Vista</span></span><br/> <span data-ttu-id="1c8dd-226">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1c8dd-226">Windows XP</span></span><br/> | <span data-ttu-id="1c8dd-227">Si le jeu utilise Direct3D, la version minimale prise en charge doit être Direct3D 9, et Direct3D doit être la valeur par défaut pour toutes les options de configuration de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-227">If the game uses Direct3D, the minimum version supported must be Direct3D 9, and Direct3D must be the default for any display configuration option.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|     <dl> <span data-ttu-id="1c8dd-228"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manuel</dt></span><span class="sxs-lookup"><span data-stu-id="1c8dd-228"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt></span></span> <dd> <span data-ttu-id="1c8dd-229">Lancez le jeu.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-229">Launch the game.</span></span> <span data-ttu-id="1c8dd-230">Dans les options vidéo, vérifiez s’il existe des options de rendu, D3D et/ou OpenGL.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-230">In the video options, check to see if there are render options, D3D and/or OpenGL.</span></span> <span data-ttu-id="1c8dd-231">Si c’est le cas, vérifiez que les options de rendu du jeu sont par défaut Direct3D.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-231">If there are, verify that the game render options default to Direct3D.</span></span> <span data-ttu-id="1c8dd-232">Si vous ne parvenez pas à vérifier que D3D9 est la version de DirectX en cours d’utilisation, passez au test automatisé.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-232">If you are unable to verify that D3D9 is the version of DirectX that is being used, then proceed to Automated Test.</span></span> <br/> </dd> <span data-ttu-id="1c8dd-233"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Test automatisé</dt></span><span class="sxs-lookup"><span data-stu-id="1c8dd-233"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automated Test</dt></span></span> <dd> <span data-ttu-id="1c8dd-234">Utiliser l’outil : Depends.exe</span><span class="sxs-lookup"><span data-stu-id="1c8dd-234">Use tool: Depends.exe</span></span> <br/> </dd> </dl> |



 

### <a name="18-enable-high-dpi-aware"></a><span data-ttu-id="1c8dd-235">1,8 activer la prise en charge des résolutions élevées</span><span class="sxs-lookup"><span data-stu-id="1c8dd-235">1.8 Enable High-DPI Aware</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c8dd-236">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c8dd-236">Windows 7</span></span><br/> <span data-ttu-id="1c8dd-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c8dd-237">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="1c8dd-238">Les jeux et leurs programmes d’installation doivent s’exécuter correctement sans problèmes visuels lorsque la mise à l’échelle DPI est activée.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-238">Games and their installers must run correctly without visual problems when DPI scaling is enabled.</span></span></td>
</tr>
<tr class="even">

<td><dl> <span data-ttu-id="1c8dd-239"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manuelle</dt> </span><span class="sxs-lookup"><span data-stu-id="1c8dd-239"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> </span></span><dd>
<ol>
<li><span data-ttu-id="1c8dd-240">Définissez le système sur PPP 150% :</span><span class="sxs-lookup"><span data-stu-id="1c8dd-240">Set the system to DPI 150%:</span></span> <br/> <span data-ttu-id="1c8dd-241">Windows Vista : panneau de configuration : personnalisation, ajuster la taille de police (DPI), résolution personnalisée.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-241">Windows Vista: Control Panel: Personalization, Adjust font size (DPI), Custom DPI.</span></span> <span data-ttu-id="1c8dd-242">Définissez sur 150%.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-242">Set to 150%.</span></span><br/> <span data-ttu-id="1c8dd-243">Windows 7 : panneau de configuration : affichage, défini sur plus de 150%.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-243">Windows 7: Control Panel: Display, Set to Larger - 150%.</span></span><br/></li>
<li><span data-ttu-id="1c8dd-244">Exécutez le processus et le jeu d’installation pour vérifier qu’il n’y a aucun problème avec les écrans détourés ou les boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-244">Run the installation process and game to verify there are no problems with clipped screens or dialog boxes.</span></span></li>
</ol>
</dd> <span data-ttu-id="1c8dd-245"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Test automatisé</dt> </span><span class="sxs-lookup"><span data-stu-id="1c8dd-245"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automated Test</dt> </span></span><dd> <span data-ttu-id="1c8dd-246">Vérifiez que l’élément <dpiAware>true</dpiAware> est contenu dans le manifeste incorporé.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-246">Verify that element <dpiAware>true</dpiAware> is contained in the embedded manifest.</span></span><br/> <span data-ttu-id="1c8dd-247">Utiliser l’outil : Mt.exe</span><span class="sxs-lookup"><span data-stu-id="1c8dd-247">Use tool: Mt.exe</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="2-security-and-compatibility"></a><span data-ttu-id="1c8dd-248">2. sécurité et compatibilité</span><span class="sxs-lookup"><span data-stu-id="1c8dd-248">2. Security and Compatibility</span></span>

### <a name="21-follow-user-account-control-guidelines"></a><span data-ttu-id="1c8dd-249">2,1 suivre les instructions relatives au contrôle de compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="1c8dd-249">2.1 Follow User Account Control Guidelines</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c8dd-250">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c8dd-250">Windows 7</span></span><br/> <span data-ttu-id="1c8dd-251">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c8dd-251">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="1c8dd-252">Chaque fichier exécutable (extension .EXE) inclus dans une application doit avoir un manifeste incorporé qui définit son niveau d’exécution :</span><span class="sxs-lookup"><span data-stu-id="1c8dd-252">Every executable file (.EXE extension) included with an application must have an embedded manifest that defines its execution level:</span></span>
<pre class="syntax" data-space="preserve"><code><requestedExecutionLevel level=&quot;asInvoker|highestAvailable|requireAdministrator&quot; 
              uiAccess=&quot;true|false&quot;/></code></pre>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1c8dd-253">Pour les jeux et les programmes d’installation de jeu, uiAccess doit toujours avoir la valeur &quot; false &quot; .</span><span class="sxs-lookup"><span data-stu-id="1c8dd-253">For games and game installers, uiAccess should always be set to &quot;false&quot;.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="1c8dd-254">Vérifiez que les fichiers exécutables de jeu contiennent des manifestes.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-254">Verify game executable files contain manifests.</span></span></li>
<li><span data-ttu-id="1c8dd-255">Vérifiez que le manifeste de fichier exécutable du jeu requestedExecutionLevel est &quot; asInvoker &quot; .</span><span class="sxs-lookup"><span data-stu-id="1c8dd-255">Verify game executable file manifest requestedExecutionLevel is &quot;AsInvoker&quot;.</span></span></li>
</ol>
<span data-ttu-id="1c8dd-256">Utiliser l’outil : Mt.exe</span><span class="sxs-lookup"><span data-stu-id="1c8dd-256">Use tool: Mt.exe</span></span> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="22-support-x64-versions-of-windows"></a><span data-ttu-id="1c8dd-257">2,2 prendre en charge les versions x64 de Windows</span><span class="sxs-lookup"><span data-stu-id="1c8dd-257">2.2 Support x64 Versions of Windows</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c8dd-258">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c8dd-258">Windows 7</span></span><br/> <span data-ttu-id="1c8dd-259">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c8dd-259">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="1c8dd-260">Pour maintenir la compatibilité avec les versions x64 de Windows :</span><span class="sxs-lookup"><span data-stu-id="1c8dd-260">To maintain compatibility with x64 versions of Windows:</span></span> <br/>
<ul>
<li><span data-ttu-id="1c8dd-261">Les programmes d’installation de titres et de titres ne doivent pas contenir de code 16 bits ou ne s’appuient sur aucun composant 16 bits.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-261">Titles and title installers must not contain any 16-bit code or rely on any 16-bit component.</span></span></li>
<li><span data-ttu-id="1c8dd-262">Si le jeu dépend des pilotes en mode noyau pour fonctionner, les versions x64 de ces pilotes doivent être disponibles.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-262">If the game is dependent on kernel-mode drivers for operation, x64 versions of these drivers must be available.</span></span> <span data-ttu-id="1c8dd-263">Le programme d’installation du jeu doit détecter et installer les pilotes et les composants appropriés pour les éditions 64 bits de Windows.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-263">The game setup must detect and install the proper drivers and components for 64-bit editions of Windows.</span></span></li>
</ul>
<blockquote>
[!Note]<br />
<span data-ttu-id="1c8dd-264">La prise en charge de l’édition 64 bits de Windows XP professionnel est facultative.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-264">Support for the 64-bit Edition of Windows XP Professional is optional.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td><span data-ttu-id="1c8dd-265">Test manuel</span><span class="sxs-lookup"><span data-stu-id="1c8dd-265">Manual Test</span></span><br/>
<ol>
<li><span data-ttu-id="1c8dd-266">Exécutez le jeu sur les éditions 64 bits de Windows.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-266">Run the game on 64-bit editions of Windows.</span></span> <span data-ttu-id="1c8dd-267">Vérifiez que le processus d’installation du jeu s’exécute normalement sur les éditions 64 bits de Windows Vista ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-267">Verify that the game installation process runs normally on 64-bit editions of Windows Vista or Windows 7.</span></span></li>
<li><span data-ttu-id="1c8dd-268">Vérifiez que le jeu ne rencontre pas d’erreur en raison d’exécutables 16 bits sur les éditions 64 bits de Windows Vista ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-268">Verify that the game does not encounter an error as a result of 16-bit executables on 64-bit editions of Windows Vista or Windows 7.</span></span> <span data-ttu-id="1c8dd-269">L’erreur indiquera l’application 16 bits dans la fenêtre d’erreur.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-269">The error will mention the 16-bit application in the error window.</span></span></li>
<li><span data-ttu-id="1c8dd-270">Si le jeu est doté d’un exécutable 64 bits natif, utilisez-le également.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-270">If the game has a native 64-bit executable, then use that as well.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="23-sign-files"></a><span data-ttu-id="1c8dd-271">2,3 fichiers de signature</span><span class="sxs-lookup"><span data-stu-id="1c8dd-271">2.3 Sign Files</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c8dd-272">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c8dd-272">Windows 7</span></span><br/> <span data-ttu-id="1c8dd-273">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c8dd-273">Windows Vista</span></span><br/> <span data-ttu-id="1c8dd-274">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1c8dd-274">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1c8dd-275">Tous les fichiers de code exécutable (par exemple, les extensions .exe et .dll) doivent être signés avec un certificat Authenticode.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-275">All executable code files (for example, .exe and .dll extensions) must be signed with an Authenticode certificate.</span></span> <br/> <span data-ttu-id="1c8dd-276">Si vous utilisez Windows Installer, les fichiers de package du programme d’installation (fichiers .msi) doivent être signés.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-276">If you are using Windows Installer, the installer's package files (.msi files) must be signed.</span></span> <br/></td>
</tr>
<tr class="even">

<td><span data-ttu-id="1c8dd-277">Test manuel</span><span class="sxs-lookup"><span data-stu-id="1c8dd-277">Manual Test</span></span><br/>
<ol>
<li><span data-ttu-id="1c8dd-278">Accédez au répertoire du jeu.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-278">Navigate to the game directory.</span></span></li>
<li><span data-ttu-id="1c8dd-279">Recherchez tous les fichiers .exe et .dll.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-279">Locate all of the .exe and .dll files.</span></span></li>
<li><span data-ttu-id="1c8dd-280">Cliquez avec le bouton droit sur Propriétés dans chaque fichier.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-280">Right-click Properties on each file.</span></span></li>
<li><span data-ttu-id="1c8dd-281">Vérifiez que les fichiers exécutables du jeu contiennent une signature numérique.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-281">Verify that the game executable files contain a digital signature.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="24-sign-drivers"></a><span data-ttu-id="1c8dd-282">2,4 signer les pilotes</span><span class="sxs-lookup"><span data-stu-id="1c8dd-282">2.4 Sign Drivers</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c8dd-283">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c8dd-283">Windows 7</span></span><br/> <span data-ttu-id="1c8dd-284">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c8dd-284">Windows Vista</span></span><br/> <span data-ttu-id="1c8dd-285">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1c8dd-285">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1c8dd-286">Tout pilote en mode noyau installé par le jeu doit être signé avec un certificat Authenticode publiquement valide.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-286">Any kernel-mode driver that is installed by the game must be signed with a publicly valid Authenticode certificate.</span></span> <br/> <span data-ttu-id="1c8dd-287">Les pilotes de périphériques matériels en mode noyau installés par le jeu doivent avoir une signature Microsoft obtenue par le biais du programme WHQL (Windows Hardware Quality Labs) ou DRS (Driver FIABILITE signature).</span><span class="sxs-lookup"><span data-stu-id="1c8dd-287">Any kernel-mode hardware device driver that is installed by the game must have a Microsoft signature obtained through the Windows Hardware Quality Labs (WHQL) or Driver Reliability Signature (DRS) program.</span></span> <br/></td>
</tr>
<tr class="even">

<td><span data-ttu-id="1c8dd-288">Test manuel</span><span class="sxs-lookup"><span data-stu-id="1c8dd-288">Manual Test</span></span><br/>
<ol>
<li><span data-ttu-id="1c8dd-289">Installez le jeu.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-289">Install the game.</span></span></li>
<li><span data-ttu-id="1c8dd-290">Vérifiez que le processus d’installation du jeu n’affiche pas de boîte (s) de dialogue de pilote non signé.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-290">Verify that the game install process does not display unsigned driver dialog(s).</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="25-perform-version-checking-properly"></a><span data-ttu-id="1c8dd-291">2,5 effectuer la vérification de la version correctement</span><span class="sxs-lookup"><span data-stu-id="1c8dd-291">2.5 Perform Version Checking Properly</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c8dd-292">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c8dd-292">Windows 7</span></span><br/> <span data-ttu-id="1c8dd-293">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c8dd-293">Windows Vista</span></span><br/> <span data-ttu-id="1c8dd-294">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1c8dd-294">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1c8dd-295">Les jeux ne peuvent pas s’exécuter sur les systèmes d’exploitation ultérieurs, comme indiqué par les modifications apportées au numéro de version de Windows, sauf si le contrat de licence utilisateur final interdit l’utilisation sur les systèmes d’exploitation ultérieurs.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-295">Games must not fail to run on future operating systems as indicated by changes in the Windows version number, unless the End User License Agreement prohibits use on future operating systems.</span></span> <span data-ttu-id="1c8dd-296">Si le jeu est supposé échouer, il doit le faire normalement en affichant un message à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-296">If the game is supposed to fail, it must do so gracefully by displaying a message to the user.</span></span></td>
</tr>
<tr class="even">

<td><dl> <span data-ttu-id="1c8dd-297"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manuelle</dt> </span><span class="sxs-lookup"><span data-stu-id="1c8dd-297"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> </span></span><dd>
<ol>
<li><span data-ttu-id="1c8dd-298">Installez le jeu sur Windows XP, sur les éditions 32 bits de Windows Vista et Windows 7, ainsi que sur les éditions 64 bits de Windows Vista et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-298">Install the game on Windows XP, on 32-bit editions of Windows Vista and Windows 7, and on 64-bit editions of Windows Vista and Windows 7.</span></span></li>
<li><span data-ttu-id="1c8dd-299">Vérifiez que le processus d’installation du jeu ne rencontre pas d’erreur concernant la version du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-299">Verify that the game installation process does not encounter an error regarding OS version.</span></span></li>
</ol>
</dd> <span data-ttu-id="1c8dd-300"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Test automatisé</dt> </span><span class="sxs-lookup"><span data-stu-id="1c8dd-300"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automated Test</dt> </span></span><dd> <span data-ttu-id="1c8dd-301">Utiliser l’outil : Application Verifier</span><span class="sxs-lookup"><span data-stu-id="1c8dd-301">Use tool: Application Verifier</span></span><br/>
<ol>
<li><span data-ttu-id="1c8dd-302">Lancez Application Verifier.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-302">Launch Application Verifier.</span></span></li>
<li><span data-ttu-id="1c8dd-303">Activez le test de compatibilité : HighVersionLie après avoir sélectionné l' INSTALL.EXE.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-303">Enable the Compatibility:HighVersionLie test after selecting the INSTALL.EXE.</span></span></li>
<li><span data-ttu-id="1c8dd-304">Installez le jeu et assurez-vous qu’il ne bloque pas l’installation en fonction de la version du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-304">Install the game and ensure that it does not block installation based on the OS version.</span></span></li>
<li><span data-ttu-id="1c8dd-305">Activez le test de compatibilité : HighVersionLie après avoir sélectionné l' GAME.EXE.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-305">Enable the Compatibility:HighVersionLie test after selecting the GAME.EXE.</span></span></li>
<li><span data-ttu-id="1c8dd-306">Exécutez le jeu et assurez-vous qu’il ne bloque pas l’exécution en fonction de la version du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-306">Run the game and ensure it does not block execution based on the OS version.</span></span></li>
</ol>
</dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="26-support-concurrent-user-sessions"></a><span data-ttu-id="1c8dd-307">2,6 prendre en charge les sessions utilisateur simultanées</span><span class="sxs-lookup"><span data-stu-id="1c8dd-307">2.6 Support Concurrent User Sessions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c8dd-308">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c8dd-308">Windows 7</span></span><br/> <span data-ttu-id="1c8dd-309">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c8dd-309">Windows Vista</span></span><br/> <span data-ttu-id="1c8dd-310">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1c8dd-310">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1c8dd-311">Les jeux doivent prendre en charge les scénarios multitâches Windows standard.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-311">Games must support standard Windows multitasking scenarios.</span></span></td>
</tr>
<tr class="even">

<td><span data-ttu-id="1c8dd-312">Créez un compte d’utilisateur standard dans Windows Vista ou Windows 7 appelé Toby.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-312">Create a Standard User account in Windows Vista or Windows 7 called Toby.</span></span> <span data-ttu-id="1c8dd-313">Démarrer-> le panneau de configuration-> ajouter ou supprimer des comptes d’utilisateur-> créer un nouveau compte</span><span class="sxs-lookup"><span data-stu-id="1c8dd-313">Start -> Control Panel -> Add or Remove User Accounts -> Create New Account</span></span> <br/>
<ol>
<li><span data-ttu-id="1c8dd-314">Lancez le jeu en tant qu’utilisateur Jane.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-314">Launch the game as User Jane.</span></span></li>
<li><span data-ttu-id="1c8dd-315">ALT + TAB de nouveau sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-315">ALT+TAB back to the desktop.</span></span></li>
<li><span data-ttu-id="1c8dd-316">Vérifiez que le jeu a correctement ALT + tabulations sur le bureau Windows.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-316">Verify that the game properly ALT+TABs to the Windows desktop.</span></span></li>
<li><span data-ttu-id="1c8dd-317">Cliquez sur Start-> [flèche à droite de LOCK]-> changer d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-317">Click Start -> [arrow to the right of Lock] -> Switch User.</span></span></li>
<li><span data-ttu-id="1c8dd-318">Ouvrez une session en tant qu’utilisateur Toby.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-318">Log on as User Toby.</span></span></li>
<li><span data-ttu-id="1c8dd-319">Vérifiez que le jeu démarre en tant qu’utilisateur Toby, tout en étant toujours en cours d’exécution en tant qu’utilisateur Jane.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-319">Verify that the game launches as User Toby while still running as User Jane.</span></span></li>
<li><span data-ttu-id="1c8dd-320">Vérifiez que le jeu ne rencontre pas d’erreurs pour l’utilisateur Toby ou l’utilisateur Jane pendant le processus de changement d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-320">Verify that the game does not encounter errors for User Toby or User Jane during User Switch process.</span></span></li>
<li><span data-ttu-id="1c8dd-321">Si vous pouvez lancer une autre session de jeu, vérifiez que vous ne pouvez pas entendre l’audio de la session de jeu d’origine.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-321">If you can launch another game session, verify that you cannot hear audio from the original game session.</span></span></li>
<li><span data-ttu-id="1c8dd-322">Fermez le jeu et revenez à l’utilisateur et au jeu d’origine.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-322">Close the game and switch back to the original user and game.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="27-support-long-names"></a><span data-ttu-id="1c8dd-323">2,7 prendre en charge les noms longs</span><span class="sxs-lookup"><span data-stu-id="1c8dd-323">2.7 Support Long Names</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c8dd-324">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c8dd-324">Windows 7</span></span><br/> <span data-ttu-id="1c8dd-325">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c8dd-325">Windows Vista</span></span><br/> <span data-ttu-id="1c8dd-326">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1c8dd-326">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1c8dd-327">Si un jeu prend en charge l’enregistrement de fichiers, il doit être en mesure d’enregistrer des fichiers avec des noms et des chemins d’accès longs.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-327">If a game supports saving files, it must be able to save files that have long names and paths.</span></span> <span data-ttu-id="1c8dd-328">Le jeu doit gérer correctement les caractères spéciaux du système de fichiers, tels que \/ : \* ?</span><span class="sxs-lookup"><span data-stu-id="1c8dd-328">The game must properly handle special file system characters, such as \ / : \* ?</span></span> <span data-ttu-id="1c8dd-329">&quot; < ou > dans les champs d’entrée utilisateur utilisés pour créer des noms de fichiers ou des chemins d’accès.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-329">&quot; < or > in any user input fields used to create file names or paths.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="1c8dd-330">Lancez le jeu.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-330">Launch the game.</span></span></li>
<li><span data-ttu-id="1c8dd-331">Démarrez un nouveau jeu.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-331">Start a new game.</span></span></li>
<li><span data-ttu-id="1c8dd-332">Enregistrez le jeu.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-332">Save the game.</span></span> <span data-ttu-id="1c8dd-333">Pendant le processus d’enregistrement, vérifiez que le jeu enregistre à l’aide de la première partie enregistrer le nom : My First Save.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-333">During the save process, verify that the game saves using the save name: My First Save Game.</span></span></li>
<li><span data-ttu-id="1c8dd-334">Revenez au menu principal.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-334">Exit back to the main menu.</span></span></li>
<li><span data-ttu-id="1c8dd-335">Essayez de charger le jeu qui vient d’être enregistré.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-335">Attempt to load the newly saved game.</span></span></li>
<li><span data-ttu-id="1c8dd-336">Vérifier que le jeu ne rencontre pas d’erreurs lors de la gestion des caractères de système de fichiers non pris en charge, tels que \/ : \* ?</span><span class="sxs-lookup"><span data-stu-id="1c8dd-336">Verify that the game does not encounter errors when handling unsupported file system characters, such as \ / : \* ?</span></span> <span data-ttu-id="1c8dd-337">&quot; < ou > si le jeu vous permet de nommer le jeu enregistré.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-337">&quot; < or > If the game allows you, name the saved game.</span></span></li>
<li><span data-ttu-id="1c8dd-338">Si l’utilisateur est autorisé à nommer son profil et/ou son caractère ou à enregistrer des parties, vérifiez que le jeu ne rencontre pas d’erreurs lors de l’utilisation de noms de fichiers longs ici également.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-338">If the user is allowed to name their profile and/or character or save games, verify that the game does not encounter errors when using long file names here as well.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="3-installation"></a><span data-ttu-id="1c8dd-339">3. installation</span><span class="sxs-lookup"><span data-stu-id="1c8dd-339">3. Installation</span></span>

### <a name="31-easy-install"></a><span data-ttu-id="1c8dd-340">Installation facile de 3,1</span><span class="sxs-lookup"><span data-stu-id="1c8dd-340">3.1 Easy Install</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c8dd-341">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c8dd-341">Windows 7</span></span><br/> <span data-ttu-id="1c8dd-342">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c8dd-342">Windows Vista</span></span><br/> <span data-ttu-id="1c8dd-343">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1c8dd-343">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1c8dd-344">Les jeux avec une installation traditionnelle doivent fournir un chemin d’accès simplifié dans leur interface utilisateur d’installation.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-344">Games with a traditional installation must provide a simplified path in their setup user interface.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="1c8dd-345">Insérez le disque du jeu.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-345">Insert the game disc.</span></span></li>
<li><span data-ttu-id="1c8dd-346">Vérifiez que le jeu n’affiche pas plus d’un contrat de licence End-User (CLUF).</span><span class="sxs-lookup"><span data-stu-id="1c8dd-346">Verify that the game does not display more than one End-User License Agreement (EULA).</span></span></li>
<li><span data-ttu-id="1c8dd-347">Si le jeu prend en charge une option d’installation personnalisée ou avancée, vérifiez que cette option est accessible pendant le processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-347">If the game supports a custom or advanced installation option, verify that this option is accessible during the installation process.</span></span></li>
<li><span data-ttu-id="1c8dd-348">Vérifiez que l’option d’installation par défaut contourne toutes les sélections d’entrée d’utilisateur pour le processus d’installation (sélection du dossier d’installation, sélection des composants, etc.).</span><span class="sxs-lookup"><span data-stu-id="1c8dd-348">Verify that the Default installation option bypasses all user input selections for the installation process (selection of installation folder, components selection, and so on).</span></span></li>
<li><span data-ttu-id="1c8dd-349">Vérifiez que le processus d’installation du jeu ne demande pas la configuration des composants du système d’exploitation (installation de DirectX, runtimes Visual C, etc.).</span><span class="sxs-lookup"><span data-stu-id="1c8dd-349">Verify that the game installation process does not prompt for OS component setup (DirectX setup, Visual C Runtimes, and so on).</span></span></li>
<li><span data-ttu-id="1c8dd-350">Vérifiez que le processus d’installation du jeu ne demande pas d’interaction avec le pare-feu.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-350">Verify that the game installation process does not prompt for firewall interaction.</span></span></li>
<li><span data-ttu-id="1c8dd-351">Vérifiez que le jeu s’exécute automatiquement ou qu’un menu de lancement est présent à la fin du processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-351">Verify that the game automatically runs or that a launcher menu is present at the end of the install process.</span></span></li>
<li><span data-ttu-id="1c8dd-352">Vérifiez que le processus de désinstallation du jeu supprime tous les fichiers installés et non redistribués des composants du système d’exploitation et efface tous les paramètres.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-352">Verify that the game uninstallation process removes all installed, non-redistributed OS component files and clears all settings.</span></span> <span data-ttu-id="1c8dd-353">Il n’est pas nécessaire de nettoyer tous les paramètres et données par utilisateur (par exemple, les parties enregistrées).</span><span class="sxs-lookup"><span data-stu-id="1c8dd-353">Cleaning up all per-user settings and data (such as saved games) is not required.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="32-support-user-account-control-for-installation"></a><span data-ttu-id="1c8dd-354">3,2 prendre en charge le contrôle de compte d’utilisateur pour l’installation</span><span class="sxs-lookup"><span data-stu-id="1c8dd-354">3.2 Support User Account Control for Installation</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c8dd-355">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c8dd-355">Windows 7</span></span><br/> <span data-ttu-id="1c8dd-356">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c8dd-356">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="1c8dd-357">Le programme d’installation du jeu ne doit pas supposer qu’il s’exécute dans le même contexte que l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-357">The game installer must not assume it is running in the same context as the user.</span></span> <span data-ttu-id="1c8dd-358">Les jeux doivent donc exécuter des tâches par utilisateur lors de la première exécution séparément de l’installation.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-358">Games must therefore perform per-user tasks on first-run separately from the installation.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="1c8dd-359">Vérifiez que vous pouvez installer le jeu en tant qu’utilisateur Jane.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-359">Verify that you can install the game as User Jane.</span></span> <span data-ttu-id="1c8dd-360">(Cela nécessite des droits élevés au cours du processus d’installation/d’installation.)</span><span class="sxs-lookup"><span data-stu-id="1c8dd-360">(This will require elevated rights during the setup/installation process.)</span></span></li>
<li><span data-ttu-id="1c8dd-361">Vérifiez que le processus d’installation du jeu invite l’utilisateur Jane à élever ses droits d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-361">Verify that the game installation process prompts User Jane to elevate through Administrator Credentials.</span></span> <span data-ttu-id="1c8dd-362">(L’invite à élever s’affiche lorsque l’utilisateur tente d’installer.)</span><span class="sxs-lookup"><span data-stu-id="1c8dd-362">(The prompt to elevate will come up when the user attempts to install.)</span></span></li>
<li><span data-ttu-id="1c8dd-363">Choisissez d’exécuter automatiquement le jeu à la fin de l’installation, s’il ne le fait pas déjà, ou lancez-le à partir du menu qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-363">Opt to Autorun the game at the end of installation, if it does not already do so, or launch it from the menu that appears.</span></span></li>
<li><span data-ttu-id="1c8dd-364">Une fois en jeu, créez un nouveau profil, jouez et enregistrez un jeu.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-364">Once in-game, create a new profile, play and save a game.</span></span></li>
<li><span data-ttu-id="1c8dd-365">Quittez le jeu.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-365">Exit the game.</span></span></li>
<li><span data-ttu-id="1c8dd-366">Redémarrez le jeu et vérifiez que les profils utilisateur et les jeux enregistrés sont accessibles par le compte utilisateur Jane.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-366">Restart the game and verify that User Profiles and Saved Games can be accessed by the User Jane account.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="33-install-to-correct-folders"></a><span data-ttu-id="1c8dd-367">3,3 installer pour corriger les dossiers</span><span class="sxs-lookup"><span data-stu-id="1c8dd-367">3.3 Install to Correct Folders</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c8dd-368">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c8dd-368">Windows 7</span></span><br/> <span data-ttu-id="1c8dd-369">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c8dd-369">Windows Vista</span></span><br/> <span data-ttu-id="1c8dd-370">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1c8dd-370">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1c8dd-371">Les jeux doivent être installés dans le dossier Program Files par défaut.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-371">Games must be installed to the Program Files folder by default.</span></span> <span data-ttu-id="1c8dd-372">Les données utilisateur doivent être écrites lors de la première exécution et non lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-372">User data must be written at first run and not during the installation.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="1c8dd-373">Installez le jeu en utilisant le type d’installation par défaut.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-373">Install the game using the Default install type.</span></span></li>
<li><span data-ttu-id="1c8dd-374">Vérifiez que le jeu a été installé dans Program Files.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-374">Verify that the game was installed to Program Files.</span></span></li>
</ol>
<blockquote>
[!Note]<br />
<span data-ttu-id="1c8dd-375">Si ce test échoue, vérifiez que le jeu est destiné à être installé pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-375">If this test fails, verify that the game is intended to install for All Users.</span></span> <span data-ttu-id="1c8dd-376">Si c’est le cas, il s’agit d’un échec.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-376">If so, this is a failure.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="34-install-windows-resources-properly"></a><span data-ttu-id="1c8dd-377">3,4 Installation des ressources Windows correctement</span><span class="sxs-lookup"><span data-stu-id="1c8dd-377">3.4 Install Windows Resources Properly</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c8dd-378">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c8dd-378">Windows 7</span></span><br/> <span data-ttu-id="1c8dd-379">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c8dd-379">Windows Vista</span></span><br/> <span data-ttu-id="1c8dd-380">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1c8dd-380">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1c8dd-381">Les applications ne doivent pas tenter d’installer des fichiers ou des clés de Registre protégés par Protection des ressources Windows (WRP).</span><span class="sxs-lookup"><span data-stu-id="1c8dd-381">Applications must not attempt to install files or registry keys that are protected by Windows Resource Protection (WRP).</span></span></td>
</tr>
<tr class="even">

<td><ul>
<li><span data-ttu-id="1c8dd-382">Vérifiez qu’aucune boîte de dialogue Protection des ressources Windows WRP ne s’affiche pendant le processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-382">Verify that no Windows Resource Protection WRP dialog boxes appear during the installation process.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="35-avoid-reboots-during-installation"></a><span data-ttu-id="1c8dd-383">3,5 éviter les redémarrages au cours de l’installation</span><span class="sxs-lookup"><span data-stu-id="1c8dd-383">3.5 Avoid Reboots During Installation</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c8dd-384">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c8dd-384">Windows 7</span></span><br/> <span data-ttu-id="1c8dd-385">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c8dd-385">Windows Vista</span></span><br/> <span data-ttu-id="1c8dd-386">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1c8dd-386">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1c8dd-387">Le programme d’installation de jeu ne doit pas supposer que l’installation de composants Windows à partir de packages de redistribution nécessite un redémarrage, sauf si le redémarrage est indiqué par un résultat de retour ou par la documentation de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-387">The game installer should not assume that installation of Windows components from redistribution packages requires a reboot, unless the reboot is indicated by a return result or by Microsoft documentation.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="1c8dd-388">Installez le jeu.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-388">Install the game.</span></span></li>
<li><span data-ttu-id="1c8dd-389">Vérifiez que le jeu ne nécessite pas le redémarrage du système après l’installation.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-389">Verify that the game does not require the system to be rebooted after installation.</span></span></li>
</ol>
<blockquote>
[!Note]<br />
<span data-ttu-id="1c8dd-390">Si un redistribution de la mise à jour Microsoft System requiert un redémarrage, procédez comme suit : terminer l’installation du jeu, désinstaller le jeu et réinstaller le jeu une deuxième fois.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-390">If a Microsoft system update REDIST requires a reboot, then do the following: Complete the game installation, uninstall the game, and reinstall the game a second time.</span></span> <span data-ttu-id="1c8dd-391">Le processus d’installation du jeu ne doit pas nécessiter un redémarrage lors de cette deuxième installation.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-391">The game installation process should not require a reboot on this second installation.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="36-use-file-versioning-correctly"></a><span data-ttu-id="1c8dd-392">3,6 utiliser le contrôle de version de fichier correctement</span><span class="sxs-lookup"><span data-stu-id="1c8dd-392">3.6 Use File Versioning Correctly</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c8dd-393">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c8dd-393">Windows 7</span></span><br/> <span data-ttu-id="1c8dd-394">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c8dd-394">Windows Vista</span></span><br/> <span data-ttu-id="1c8dd-395">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1c8dd-395">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1c8dd-396">Le programme d’installation du jeu doit vérifier correctement si les dernières versions de fichiers sont installées.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-396">The game installation program must properly check to ensure that the latest file versions are installed.</span></span> <span data-ttu-id="1c8dd-397">L’installation d’un jeu ne doit jamais régresser les fichiers que vous ne générez pas ou qui sont partagés par des applications que vous ne générez pas.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-397">Installing a game must never regress any files that you do not produce or that are shared by applications that you do not produce.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="1c8dd-398">Avant d’installer le jeu, créez une capture instantanée de préinstallation de system32.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-398">Prior to installing the game, create a pre-install snapshot of System32.</span></span><br/>
<ol>
<li><span data-ttu-id="1c8dd-399">Créez un répertoire appelé G4Wtest.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-399">Make a directory called G4Wtest.</span></span></li>
<li><span data-ttu-id="1c8dd-400">Afficher une fenêtre de commande (Start-> Run-> cmd).</span><span class="sxs-lookup"><span data-stu-id="1c8dd-400">Bring up a command Window (Start -> Run -> cmd).</span></span></li>
<li><span data-ttu-id="1c8dd-401">Accédez à c:\Windows\System32.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-401">Navigate to c:\windows\system32.</span></span></li>
<li><span data-ttu-id="1c8dd-402">Tapez dir/o :-g/o :-d >> c:\G4Wtest\pregame.txt.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-402">Type dir /o:-g /o:-d >> c:\G4Wtest\pregame.txt.</span></span></li>
</ol></li>
<li><span data-ttu-id="1c8dd-403">Créez un instantané postérieur à l’installation de system32.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-403">Create a post-install snapshot of System32.</span></span> <br/>
<ol>
<li><span data-ttu-id="1c8dd-404">Afficher une fenêtre de commande (Start-> Run-> cmd).</span><span class="sxs-lookup"><span data-stu-id="1c8dd-404">Bring up a command Window (Start -> Run -> cmd).</span></span></li>
<li><span data-ttu-id="1c8dd-405">Accédez à c:\Windows\System32.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-405">Navigate to c:\windows\system32.</span></span></li>
<li><span data-ttu-id="1c8dd-406">Tapez dir/o :-g/o :-d >> c:\G4Wtest\postgame.txt.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-406">Type dir /o:-g /o:-d >> c:\G4Wtest\postgame.txt.</span></span></li>
<li><span data-ttu-id="1c8dd-407">Vérifiez que le jeu n’a pas pour effet de régresser les versions de fichiers que le jeu n’a pas produit (... des fichiers figurant dans les deux documents en comparant pregame.txt à postgame.txt).</span><span class="sxs-lookup"><span data-stu-id="1c8dd-407">Verify that the game does not regress any file versions of files that the game did not produce (...of the files listed in the two documents by comparing pregame.txt to postgame.txt).</span></span></li>
</ol></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="37-support-autorun-conditional-requirement"></a><span data-ttu-id="1c8dd-408">3,7 prise en charge de l’exigence conditionnelle d’exécution automatique \[\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-408">3.7 Support Autorun \[Conditional Requirement\]</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c8dd-409">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c8dd-409">Windows 7</span></span><br/> <span data-ttu-id="1c8dd-410">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c8dd-410">Windows Vista</span></span><br/> <span data-ttu-id="1c8dd-411">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1c8dd-411">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1c8dd-412">Pour les jeux distribués sur CD, DVD ou tout autre support amovible qui prennent en charge l’exécution automatique, lorsque le disque est inséré pour la première fois, l’application doit automatiquement s’exécuter ou inviter l’utilisateur à installer le jeu.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-412">For games distributed on CD, DVD, or other removable media that support Autorun, when the disc is inserted for the first time, the application must automatically run or prompt the user to install the game.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1c8dd-413">Les programmes d’exécution automatique qui ont été écrits pour une utilisation sur des versions de Windows antérieures à Windows Vista ne doivent pas utiliser le Runtime .NET, car cette technologie n’est pas fournie avec Windows XP ou des versions antérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-413">Autorun programs that were written for use on versions of Windows prior to Windows Vista should not use the .NET runtime, because this technology is not included with Windows XP or older versions of Windows.</span></span>
</blockquote>
<br/> <span data-ttu-id="1c8dd-414">Pour plus d’informations, reportez-vous à <a href="/windows/win32/DxTechArts/games-for-windows-technical-requirements-1-1-0006">jeux pour les exigences techniques Windows</a> 3,7, support autorun.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-414">For further guidance, please refer to <a href="/windows/win32/DxTechArts/games-for-windows-technical-requirements-1-1-0006">Games for Windows Technical Requirements</a> 3.7, Support Autorun.</span></span> <br/></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="1c8dd-415">Insérez le disque ou le média du jeu.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-415">Insert the game disc or media.</span></span></li>
<li><span data-ttu-id="1c8dd-416">Vérifiez que la boîte de dialogue installation/exécution s’affiche automatiquement.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-416">Verify that the install / run dialog box comes up automatically.</span></span></li>
<li><span data-ttu-id="1c8dd-417">Windows Vista ou Windows 7 : Vérifiez que le programme d’exécution automatique de jeu lui-même ne demande pas à l’utilisateur Jane d’élever les informations d’identification d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-417">Windows Vista or Windows 7: Verify that the game Autorun program itself does not prompt User Jane to elevate through Administrator Credentials.</span></span></li>
<li><span data-ttu-id="1c8dd-418">Vérifiez que l’exécutable d’exécution automatique n’a pas besoin de composants de redistribution out-of-Box, tels que les bibliothèques .NET 3,5, C Run-Time, etc.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-418">Verify that the Autorun executable doesn't need out-of-box REDIST components, such as .NET 3.5, C Run-Time libraries, and so on.</span></span></li>
<li><span data-ttu-id="1c8dd-419">Vérifiez que la réinsertion du disque dans le lecteur après l’installation n’entraîne pas le redémarrage automatique de l’installation.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-419">Verify that re-inserting the disc in the drive after installation does not cause installation to automatically begin again.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="4-reliability"></a><span data-ttu-id="1c8dd-420">4. fiabilité</span><span class="sxs-lookup"><span data-stu-id="1c8dd-420">4. Reliability</span></span>

### <a name="41-eliminate-unnecessary-reboots"></a><span data-ttu-id="1c8dd-421">4,1 éliminer les redémarrages inutiles</span><span class="sxs-lookup"><span data-stu-id="1c8dd-421">4.1 Eliminate Unnecessary Reboots</span></span>



| <span data-ttu-id="1c8dd-422">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="1c8dd-422">OS</span></span>                                              | <span data-ttu-id="1c8dd-423">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c8dd-423">Requirement</span></span>                                                                                                                                                                   |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c8dd-424">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c8dd-424">Windows 7</span></span><br/> <span data-ttu-id="1c8dd-425">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c8dd-425">Windows Vista</span></span><br/> | <span data-ttu-id="1c8dd-426">Tous les programmes d’installation de l’application doivent tirer parti des API du gestionnaire de redémarrage pour éviter les redémarrages du système (voir la [condition 3,5](#35-avoid-reboots-during-installation)).</span><span class="sxs-lookup"><span data-stu-id="1c8dd-426">All application installers must take advantage of the Restart Manager APIs to avoid system reboots (see [requirement 3.5](#35-avoid-reboots-during-installation)).</span></span> |



 

### <a name="42-eliminate-application-verifier-failures"></a><span data-ttu-id="1c8dd-427">4,2 éliminer les échecs de Application Verifier</span><span class="sxs-lookup"><span data-stu-id="1c8dd-427">4.2 Eliminate Application Verifier Failures</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c8dd-428">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c8dd-428">Windows 7</span></span><br/> <span data-ttu-id="1c8dd-429">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c8dd-429">Windows Vista</span></span><br/> <span data-ttu-id="1c8dd-430">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1c8dd-430">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1c8dd-431">Le jeu ne doit générer aucun échec s’exécutant sous Microsoft Application Verifier (AppVerifier), version 4,0 ou ultérieure, dans les tests suivants :</span><span class="sxs-lookup"><span data-stu-id="1c8dd-431">The game must generate no failures running under Microsoft Application Verifier (AppVerifier), version 4.0 or later, in the following tests:</span></span> <br/>
<ul>
<li><span data-ttu-id="1c8dd-432">Concepts de base : handles, tas, verrous, mémoire, TLS</span><span class="sxs-lookup"><span data-stu-id="1c8dd-432">Basics: Handles, Heaps, Locks, Memory, TLS</span></span></li>
<li><span data-ttu-id="1c8dd-433">Divers : DangerousAPIs, DirtyStacks</span><span class="sxs-lookup"><span data-stu-id="1c8dd-433">Miscellaneous: DangerousAPIs, DirtyStacks</span></span></li>
</ul></td>
</tr>
<tr class="even">

<td><span data-ttu-id="1c8dd-434">Utiliser l’outil : AppVerifier 4,0 (ou version ultérieure)</span><span class="sxs-lookup"><span data-stu-id="1c8dd-434">Use Tool: AppVerifier 4.0 (or later)</span></span><br/>
<ol>
<li><span data-ttu-id="1c8dd-435">Installer AppVerifier.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-435">Install AppVerifier.</span></span></li>
<li><span data-ttu-id="1c8dd-436">Lancez AppVerifier et sélectionnez fichier-> ajouter une application.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-436">Launch AppVerifier and select File -> Add Application.</span></span></li>
<li><span data-ttu-id="1c8dd-437">Recherchez l’exécutable du jeu, sélectionnez-le, puis cliquez sur le &quot; &quot; bouton Ouvrir.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-437">Locate the game executable, select it, and click the &quot;Open&quot; button.</span></span></li>
<li><span data-ttu-id="1c8dd-438">Dans la &quot; &quot; section applications, sélectionnez l’exécutable du jeu.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-438">In the &quot;Applications&quot; section, select the game executable.</span></span></li>
<li><span data-ttu-id="1c8dd-439">Dans la &quot; &quot; section tests, sélectionnez les tests répertoriés ci-dessus sous les catégories &quot; concepts &quot; de base et &quot; divers &quot; (décochez ThreadPool et TimeRollOver) et vérifiez que tous les autres tests ne sont pas sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-439">In the &quot;Tests&quot; section, select the tests listed above under the categories &quot;Basics&quot; and &quot;Miscellaneous&quot; (uncheck ThreadPool and TimeRollOver), and ensure all other tests are not selected.</span></span></li>
<li><span data-ttu-id="1c8dd-440">Lancez le jeu.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-440">Launch the game.</span></span></li>
<li><span data-ttu-id="1c8dd-441">Vérifiez que le jeu ne génère pas d’erreurs lorsqu’il est exécuté sous Application Verifier.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-441">Verify that the game does not generate failures when run under Application Verifier.</span></span></li>
</ol>
<blockquote>
[!Note]<br />
<span data-ttu-id="1c8dd-442">Certains tests requièrent l’exécution complète d’un débogueur.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-442">Some tests require a debugger to be fully run.</span></span> <span data-ttu-id="1c8dd-443">Cela peut nécessiter une version non protégée de l’exécutable du jeu, car la technologie anti-triche/anti-piratage peut interférer avec AppVerifer.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-443">This may require an unprotected release version of the game executable, since anti-cheat/anti-piracy technology may interfere with AppVerifer.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="43-support-windows-error-reporting"></a><span data-ttu-id="1c8dd-444">Rapport d’erreurs Windows de support 4,3</span><span class="sxs-lookup"><span data-stu-id="1c8dd-444">4.3 Support Windows Error Reporting</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c8dd-445">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c8dd-445">Windows 7</span></span><br/> <span data-ttu-id="1c8dd-446">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c8dd-446">Windows Vista</span></span><br/> <span data-ttu-id="1c8dd-447">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1c8dd-447">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1c8dd-448">Les jeux doivent gérer uniquement les exceptions connues et attendues, et la Rapport d’erreurs Windows ne doit pas être désactivée.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-448">Games must handle only exceptions that are known and expected, and Windows Error Reporting must not be disabled.</span></span> <span data-ttu-id="1c8dd-449">Si une erreur (telle qu’une violation d’accès) est injectée dans un jeu, elle doit autoriser Rapport d’erreurs Windows à signaler l’incident.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-449">If a fault (such as an Access Violation) is injected into a game, it must allow Windows Error Reporting to report the crash.</span></span></td>
</tr>
<tr class="even">

<td><span data-ttu-id="1c8dd-450">Utiliser l’outil : détourneur de thread</span><span class="sxs-lookup"><span data-stu-id="1c8dd-450">Use Tool: Thread Hijacker</span></span> <br/>
<ul>
<li><span data-ttu-id="1c8dd-451">Si l’application se bloque pendant le test, vérifiez que le jeu affiche Rapport d’erreurs Windows correctement et collecte des données de panne.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-451">If the application crashes while testing, verify that the game displays Windows Error Reporting properly and collects crash data.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c8dd-452">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c8dd-452">Windows 7</span></span><br/> <span data-ttu-id="1c8dd-453">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c8dd-453">Windows Vista</span></span><br/> <span data-ttu-id="1c8dd-454">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1c8dd-454">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1c8dd-455">Tous les fichiers exécutables (par exemple, les fichiers .exe ou .dll) doivent contenir un nom de produit, un nom de société et une version de fichier précis.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-455">All executable files (for example, .exe or .dll files) must contain an accurate Product Name, Company Name, and File Version.</span></span></td>
</tr>
<tr class="even">

<td><dl> <span data-ttu-id="1c8dd-456"><dt><span id="Manual_test_"></span><span id="manual_test_"></span><span id="MANUAL_TEST_"></span>Test manuel :</dt> </span><span class="sxs-lookup"><span data-stu-id="1c8dd-456"><dt><span id="Manual_test_"></span><span id="manual_test_"></span><span id="MANUAL_TEST_"></span>Manual test:</dt> </span></span><dd>
<ol>
<li><span data-ttu-id="1c8dd-457">Cliquez avec le bouton droit sur le ou les fichiers exécutables du jeu sur le support d’installation de et sur ceux qui sont installés sur le disque dur de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-457">Right-click the game's executable file(s) on both the installation media and those installed to the computer hard drive.</span></span></li>
<li><span data-ttu-id="1c8dd-458">Sélectionnez Propriétés.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-458">Select Properties.</span></span></li>
<li><span data-ttu-id="1c8dd-459">Windows XP : cliquez sur l’onglet <strong>version</strong> . Vérifiez que les champs nom du produit, nom de la société et version du fichier sont correctement remplis.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-459">Windows XP: Click the <strong>Version</strong> tab. Verify that the Product Name, Company Name, and File Version fields are properly populated.</span></span></li>
<li><span data-ttu-id="1c8dd-460">Windows Vista ou Windows 7 : cliquez sur l’onglet <strong>Détails</strong> . Vérifiez que les champs nom du produit et version du fichier sont correctement remplis.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-460">Windows Vista or Windows 7: Click the <strong>Details</strong> tab. Verify that the Product name and File Version fields are properly populated.</span></span> <span data-ttu-id="1c8dd-461">Le nom de la société n’est pas visible dans la page Propriétés de Windows Vista ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-461">Company Name is not visible in the Windows Vista or Windows 7 properties page.</span></span></li>
</ol>
</dd> <span data-ttu-id="1c8dd-462"><dt><span id="Automated_test_"></span><span id="automated_test_"></span><span id="AUTOMATED_TEST_"></span>Test automatisé :</dt> </span><span class="sxs-lookup"><span data-stu-id="1c8dd-462"><dt><span id="Automated_test_"></span><span id="automated_test_"></span><span id="AUTOMATED_TEST_"></span>Automated test:</dt> </span></span><dd>
<ul>
<li><span data-ttu-id="1c8dd-463">Utilisez l’outil de test Microsoft Games for Windows. consultez la <a href="#64-microsoft-games-for-windows-test-tool">section 6,4</a>.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-463">Use the Microsoft Games for Windows Test Tool; see <a href="#64-microsoft-games-for-windows-test-tool">section 6.4</a>.</span></span></li>
</ul>
</dd> </dl></td>
</tr>
</tbody>
</table>



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c8dd-464">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c8dd-464">Windows 7</span></span><br/> <span data-ttu-id="1c8dd-465">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c8dd-465">Windows Vista</span></span><br/> <span data-ttu-id="1c8dd-466">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1c8dd-466">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1c8dd-467">La sortie normale du jeu ne doit pas aboutir à une erreur d’exception inconnue.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-467">Normal exit of the game must not result in an unknown exception fault.</span></span></td>
</tr>
<tr class="even">

<td><ul>
<li><span data-ttu-id="1c8dd-468">Après avoir joué le jeu pour une session de jeu normale, vérifiez que le jeu ne génère pas d’erreurs à la sortie.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-468">After playing the game for a normal gaming session, verify that the game does not generate errors on exit.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="5-sample-test-script"></a><span data-ttu-id="1c8dd-469">5. exemple de script de test</span><span class="sxs-lookup"><span data-stu-id="1c8dd-469">5. Sample Test Script</span></span>

<span data-ttu-id="1c8dd-470">Il s’agit d’un exemple de test typique en utilisant les exigences de test ci-dessus comme guide.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-470">This is an example of a typical test pass using the preceding test requirements as a guide.</span></span>

### <a name="51-tools"></a><span data-ttu-id="1c8dd-471">5,1 outils</span><span class="sxs-lookup"><span data-stu-id="1c8dd-471">5.1 Tools</span></span>

-   <span data-ttu-id="1c8dd-472">édition 32 bits de Windows Vista SP1 et/ou Windows 7 sur un processeur AMD</span><span class="sxs-lookup"><span data-stu-id="1c8dd-472">32-bit edition of Windows Vista SP1 and/or Windows 7 on an AMD CPU</span></span>
-   <span data-ttu-id="1c8dd-473">édition 32 bits de Windows Vista SP1 et/ou Windows 7 sur un processeur Intel</span><span class="sxs-lookup"><span data-stu-id="1c8dd-473">32-bit edition of Windows Vista SP1 and/or Windows 7 on an Intel CPU</span></span>
-   <span data-ttu-id="1c8dd-474">édition 64 bits de Windows Vista SP1 et/ou Windows 7 sur un processeur AMD</span><span class="sxs-lookup"><span data-stu-id="1c8dd-474">64-bit edition of Windows Vista SP1 and/or Windows 7 on an AMD CPU</span></span>
-   <span data-ttu-id="1c8dd-475">édition 64 bits de Windows Vista SP1 et/ou Windows 7 sur un processeur Intel</span><span class="sxs-lookup"><span data-stu-id="1c8dd-475">64-bit edition of Windows Vista SP1 and/or Windows 7 on an Intel CPU</span></span>
-   <span data-ttu-id="1c8dd-476">édition 32 bits de Windows XP SP2 sur un processeur AMD</span><span class="sxs-lookup"><span data-stu-id="1c8dd-476">32-bit edition Windows XP SP2 on an AMD CPU</span></span>
-   <span data-ttu-id="1c8dd-477">édition 32 bits de Windows XP SP2 sur un processeur Intel</span><span class="sxs-lookup"><span data-stu-id="1c8dd-477">32-bit edition Windows XP SP2 on an Intel CPU</span></span>
-   <span data-ttu-id="1c8dd-478">Moniteur à écran étendu qui prend en charge 1680 1050</span><span class="sxs-lookup"><span data-stu-id="1c8dd-478">Wide Screen Monitor that supports 1680 1050</span></span>
-   <span data-ttu-id="1c8dd-479">Contrôleur Xbox 360 pour Windows</span><span class="sxs-lookup"><span data-stu-id="1c8dd-479">Xbox 360 Controller for Windows</span></span>

### <a name="52-pre-install"></a><span data-ttu-id="1c8dd-480">5,2 pré-installation</span><span class="sxs-lookup"><span data-stu-id="1c8dd-480">5.2 Pre-Install</span></span>

1.  <span data-ttu-id="1c8dd-481">Windows Vista et Windows 7 : créez deux utilisateurs standard : Jane et Toby</span><span class="sxs-lookup"><span data-stu-id="1c8dd-481">Windows Vista and Windows 7: Create two Standard Users: Jane and Toby</span></span>
2.  <span data-ttu-id="1c8dd-482">Windows Vista et Windows 7 : vérifier que le contrôle de compte d’utilisateur est activé</span><span class="sxs-lookup"><span data-stu-id="1c8dd-482">Windows Vista and Windows 7: Ensure User Account Control is enabled</span></span>
3.  <span data-ttu-id="1c8dd-483">Créer un instantané de préinstallation de system32</span><span class="sxs-lookup"><span data-stu-id="1c8dd-483">Create a pre-install snapshot of System32</span></span>

    1.  <span data-ttu-id="1c8dd-484">Créer un répertoire appelé G4Wtest</span><span class="sxs-lookup"><span data-stu-id="1c8dd-484">Make a directory called G4Wtest</span></span>
    2.  <span data-ttu-id="1c8dd-485">Afficher une fenêtre de commande (Start-> Run-> cmd)</span><span class="sxs-lookup"><span data-stu-id="1c8dd-485">Bring up a command Window (Start -> Run -> cmd)</span></span>
    3.  <span data-ttu-id="1c8dd-486">Accédez à c : \\ Windows \\ system32</span><span class="sxs-lookup"><span data-stu-id="1c8dd-486">Navigate to c:\\windows\\system32</span></span>
    4.  <span data-ttu-id="1c8dd-487">Tapez dir/o :-g/o :-d >> c : \\ G4Wtest \\pregame.txt</span><span class="sxs-lookup"><span data-stu-id="1c8dd-487">Type dir /o:-g /o:-d >> c:\\G4Wtest\\pregame.txt</span></span>

4.  <span data-ttu-id="1c8dd-488">Windows Vista et Windows 7 : définir sur 150% ppp \[ 1,8\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-488">Windows Vista and Windows 7: Set to 150% DPI \[1.8\]</span></span>
5.  <span data-ttu-id="1c8dd-489">Continuer l' [installation](#3-installation)</span><span class="sxs-lookup"><span data-stu-id="1c8dd-489">Proceed to [Install](#3-installation)</span></span>

### <a name="53-install"></a><span data-ttu-id="1c8dd-490">installation de 5,3</span><span class="sxs-lookup"><span data-stu-id="1c8dd-490">5.3 Install</span></span>

1.  <span data-ttu-id="1c8dd-491">Ouvrir une session en tant qu’utilisateur Jane</span><span class="sxs-lookup"><span data-stu-id="1c8dd-491">Log on as User Jane</span></span>
2.  <span data-ttu-id="1c8dd-492">Insérez le disque du jeu dans le lecteur de CD/DVD, vérifiez que la boîte de dialogue installation/exécution s’affiche automatiquement \[ 3,7\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-492">Insert the game disc into the CD/DVD drive, verify that the install / run dialog box comes up automatically \[3.7\]</span></span>
3.  <span data-ttu-id="1c8dd-493">Vérifiez que le processus d’installation du jeu invite l’utilisateur Jane à élever les informations d’identification de l’administrateur \[ 3,2\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-493">Verify that the game installation process prompts User Jane to elevate Administrator Credentials \[3.2\]</span></span>
4.  <span data-ttu-id="1c8dd-494">Vérifiez que le programme d’exécution automatique de jeu lui-même ne demande pas à l’utilisateur Jane d’effectuer une élévation via les informations d’identification d’administrateur \[ 3,7\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-494">Verify that the game Autorun program itself does not prompt User Jane to elevate through Administrator Credentials \[3.7\]</span></span>
5.  <span data-ttu-id="1c8dd-495">Vérifiez que le jeu n’affiche pas plus d’un contrat de licence End-User (CLUF) \[ 3,1\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-495">Verify that the game does not display more than one End-User License Agreement (EULA) \[3.1\]</span></span>
6.  <span data-ttu-id="1c8dd-496">Vérifiez que le jeu affiche les options d’installation par défaut/simples et personnalisées/avancées \[ 3,1\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-496">Verify that the game displays Default/Easy and Custom/Advanced installation options \[3.1\]</span></span>
7.  <span data-ttu-id="1c8dd-497">Vérifiez que l’option d’installation par défaut/Easy contourne toutes les sélections d’entrée utilisateur pour le processus d’installation (sélection du dossier d’installation, sélection des composants, etc.) \[ . 3,1\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-497">Verify that the Default/Easy installation option bypasses all user input selections for the install process (selection of installation folder, components selection, and so on.) \[3.1\]</span></span>
8.  <span data-ttu-id="1c8dd-498">Vérifiez que le processus d’installation du jeu ne demande pas la configuration des composants du système d’exploitation (installation de DirectX, bibliothèques C Run-Time, etc.) \[ . 3,1\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-498">Verify that the game installation process does not prompt for OS component setup (DirectX setup, C Run-Time libraries, and so on.) \[3.1\]</span></span>
9.  <span data-ttu-id="1c8dd-499">Vérifier que le processus d’installation du jeu ne demande pas d’interaction avec le pare-feu \[ 3,1\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-499">Verify that the game installation process does not prompt for firewall interaction \[3.1\]</span></span>
10. <span data-ttu-id="1c8dd-500">Vérifiez que le processus d’installation du jeu ne rencontre pas d’erreur concernant la version \[ 2,5 \] \[ 4,2 du système d’exploitation\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-500">Verify that the game installation process does not encounter an error regarding OS Version \[2.5\] \[4.2\]</span></span>
11. <span data-ttu-id="1c8dd-501">Vérifiez que le processus d’installation du jeu n’affiche pas de boîte (s) de dialogue de pilote non signé \[ 2,4\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-501">Verify that the game installation process does not display unsigned driver dialog(s) \[2.4\]</span></span>
12. <span data-ttu-id="1c8dd-502">Vérifiez qu’aucune boîte de dialogue de Protection des ressources Windows (WRP) ne s’affiche pendant le processus d’installation \[ 3,4\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-502">Verify that no Windows Resource Protection (WRP) dialogs appear during the install process \[3.4\]</span></span>
13. <span data-ttu-id="1c8dd-503">Vérifiez que la réinsertion du disque dans le lecteur après l’installation n’entraîne pas le redémarrage automatique de l’installation</span><span class="sxs-lookup"><span data-stu-id="1c8dd-503">Verify that re-inserting the disc in the drive after installation does not cause installation to automatically begin again</span></span>
14. <span data-ttu-id="1c8dd-504">Vérifiez que le jeu ne nécessite pas le redémarrage du système après l’installation \[ 3,5\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-504">Verify that the game does not require the system to be rebooted after installation \[3.5\]</span></span>
15. <span data-ttu-id="1c8dd-505">Vérifiez que vous pouvez installer le jeu en tant qu’utilisateur Jane \[ 3,2\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-505">Verify that you can install the game as User Jane \[3.2\]</span></span>
16. <span data-ttu-id="1c8dd-506">Vérifiez que le jeu s’exécute automatiquement ou qu’un menu de lancement est présent à la fin du processus d’installation \[ 3,1\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-506">Verify that the game automatically runs or that a launcher menu is present at the end of the installation process \[3.1\]</span></span>
17. <span data-ttu-id="1c8dd-507">Si le jeu s’exécute automatiquement après l’installation, passez au [Runtime](#55-runtime)</span><span class="sxs-lookup"><span data-stu-id="1c8dd-507">If the game does auto-run after installation, skip to [Runtime](#55-runtime)</span></span>
18. <span data-ttu-id="1c8dd-508">Si le jeu a quitté un menu de lancement ou n’a pas pu désinstaller, voir la section [après l’installation](#54-post-install)</span><span class="sxs-lookup"><span data-stu-id="1c8dd-508">If the game left a launch menu up, or failed to uninstall see section [Post-Install](#54-post-install)</span></span>

### <a name="54-post-install"></a><span data-ttu-id="1c8dd-509">5,4 après l’installation</span><span class="sxs-lookup"><span data-stu-id="1c8dd-509">5.4 Post-Install</span></span>

1.  <span data-ttu-id="1c8dd-510">Vérifier que le jeu ne place pas de raccourcis de lancement sur le Bureau de l’utilisateur \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-510">Verify that the game does not place launch shortcuts on user desktop \[1.1\]</span></span>
2.  <span data-ttu-id="1c8dd-511">Vérifiez que le jeu ne place pas de raccourcis de lancement dans le menu démarrer \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-511">Verify that the game does not place launch shortcuts in the Start Menu \[1.1\]</span></span>
3.  <span data-ttu-id="1c8dd-512">Vérifiez que l’icône de jeu s’affiche dans l’Explorateur Windows Jeux \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-512">Verify that the game icon displays in Windows Games Explorer \[1.1\]</span></span>
4.  <span data-ttu-id="1c8dd-513">Vérifiez que les métadonnées (éditeur, développeur, genre, date de publication, version) s’affichent en bas et qu’elles sont correctes. \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-513">Verify that the metadata (publisher, developer, genre, release date, version) at the bottom displays and is correct \[1.1\]</span></span>
5.  <span data-ttu-id="1c8dd-514">Vérifiez que l’icône du jeu affiche des informations sur l’indice de performance Windows (WEI) dans l’Explorateur de jeux Windows \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-514">Verify that the game icon displays Windows Experience Index (WEI) information in Windows Games Explorer \[1.1\]</span></span>
6.  <span data-ttu-id="1c8dd-515">Vérifier que les liens hypertexte de jeu pour les métadonnées fonctionnent correctement dans l’Explorateur de jeux Windows \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-515">Verify that game hyperlinks for metadata work correctly in Windows Games Explorer \[1.1\]</span></span>
7.  <span data-ttu-id="1c8dd-516">Vérifier que le jeu affiche une évaluation précise du contrôle parental dans l’Explorateur de jeux Windows \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-516">Verify that the game displays accurate parental control rating in Windows Games Explorer \[1.1\]</span></span>
8.  <span data-ttu-id="1c8dd-517">Créer un instantané postérieur à l’installation de system32</span><span class="sxs-lookup"><span data-stu-id="1c8dd-517">Create a post-install snapshot of System32</span></span>

    1.  <span data-ttu-id="1c8dd-518">Afficher une fenêtre de commande (Start-> Run-> cmd)</span><span class="sxs-lookup"><span data-stu-id="1c8dd-518">Bring up a command Window (Start -> Run -> cmd)</span></span>
    2.  <span data-ttu-id="1c8dd-519">Accédez à c : \\ Windows \\ system32</span><span class="sxs-lookup"><span data-stu-id="1c8dd-519">Navigate to c:\\windows\\system32</span></span>
    3.  <span data-ttu-id="1c8dd-520">Tapez dir/o :-g/o :-d >> c : \\ G4Wtest \\postgame.txt</span><span class="sxs-lookup"><span data-stu-id="1c8dd-520">Type dir /o:-g /o:-d >> c:\\G4Wtest\\postgame.txt</span></span>
    4.  <span data-ttu-id="1c8dd-521">Vérifiez que le jeu ne régresse pas les versions de fichiers listées dans les deux documents en comparant pregame.txt à postgame.txt \[ 3,6\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-521">Verify that the game does not regress any file versions of files listed in the two documents by comparing pregame.txt to postgame.txt \[3.6\]</span></span>

9.  <span data-ttu-id="1c8dd-522">Passer au [Runtime](#55-runtime)</span><span class="sxs-lookup"><span data-stu-id="1c8dd-522">Proceed to [Runtime](#55-runtime)</span></span>

### <a name="55-runtime"></a><span data-ttu-id="1c8dd-523">Runtime 5,5</span><span class="sxs-lookup"><span data-stu-id="1c8dd-523">5.5 Runtime</span></span>

1.  <span data-ttu-id="1c8dd-524">RUNTIME 1 : si le menu de lancement est présent, lancez le jeu à partir de là.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-524">RUNTIME 1: If the launch menu is present, launch the game from there.</span></span> <span data-ttu-id="1c8dd-525">Si le jeu a été exécuté automatiquement ou a été lancé à partir du menu du lanceur de jeux après l’installation, procédez comme suit : Si ce n’est pas le cas, passez au RUNTIME 2 :</span><span class="sxs-lookup"><span data-stu-id="1c8dd-525">If the game auto-ran or was launched from the game launcher menu after install, perform the following; if not, skip to RUNTIME 2:</span></span>

    1.  <span data-ttu-id="1c8dd-526">Créer un profil (si le jeu le permet)</span><span class="sxs-lookup"><span data-stu-id="1c8dd-526">Create a profile (if the game allows)</span></span>
    2.  <span data-ttu-id="1c8dd-527">Démarrer un nouveau jeu</span><span class="sxs-lookup"><span data-stu-id="1c8dd-527">Start a new game</span></span>
    3.  <span data-ttu-id="1c8dd-528">Enregistrer le jeu</span><span class="sxs-lookup"><span data-stu-id="1c8dd-528">Save the game</span></span>
    4.  <span data-ttu-id="1c8dd-529">Quitter le jeu</span><span class="sxs-lookup"><span data-stu-id="1c8dd-529">Exit the game</span></span>
    5.  <span data-ttu-id="1c8dd-530">Lancer le jeu à partir de l’Explorateur de jeux</span><span class="sxs-lookup"><span data-stu-id="1c8dd-530">Launch the game from Games Explorer</span></span>
    6.  <span data-ttu-id="1c8dd-531">Vérifier que le jeu est lancé à partir de l’icône de l’Explorateur de jeux \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-531">Verify that the game launches from the Games Explorer icon \[1.2\]</span></span>
    7.  <span data-ttu-id="1c8dd-532">Vérifiez que le jeu ne demande pas les informations d’identification de l’administrateur au lancement de \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-532">Verify that the game does not prompt for Administrator Credentials on launch \[1.2\]</span></span>
    8.  <span data-ttu-id="1c8dd-533">Vérifier que les profils utilisateur et l’enregistrement des jeux sont accessibles par l’utilisateur Jane compte \[ 3,2\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-533">Verify that User Profiles and Save Games can be accessed by User Jane account \[3.2\]</span></span>
    9.  <span data-ttu-id="1c8dd-534">Passer au RUNTIME 3</span><span class="sxs-lookup"><span data-stu-id="1c8dd-534">Proceed to RUNTIME 3</span></span>

2.  <span data-ttu-id="1c8dd-535">RUNTIME 2 : si le jeu n’a pas été exécuté automatiquement ou si vous affichez un lancement à partir du menu du lanceur de jeu, il s’agit d’une défaillance de \[ 3,1 \] ; Toutefois, le test peut se poursuivre normalement :</span><span class="sxs-lookup"><span data-stu-id="1c8dd-535">RUNTIME 2: If the game did not auto-run or display a launch from the game launcher menu, this is a failure of \[3.1\]; however, testing can continue normally:</span></span>

    1.  <span data-ttu-id="1c8dd-536">Lancer le jeu à partir de l’Explorateur de jeux</span><span class="sxs-lookup"><span data-stu-id="1c8dd-536">Launch the game from Games Explorer</span></span>
    2.  <span data-ttu-id="1c8dd-537">Vérifier que le jeu est lancé à partir de l’icône de l’Explorateur de jeux \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-537">Verify that the game launches from the Games Explorer icon \[1.2\]</span></span>
    3.  <span data-ttu-id="1c8dd-538">Vérifiez que le jeu ne demande pas les informations d’identification de l’administrateur au lancement de \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-538">Verify that the game does not prompt for Administrator Credentials on launch \[1.2\]</span></span>
    4.  <span data-ttu-id="1c8dd-539">Passer au RUNTIME 3</span><span class="sxs-lookup"><span data-stu-id="1c8dd-539">Proceed to RUNTIME 3</span></span>

3.  <span data-ttu-id="1c8dd-540">RUNTIME 3 : si le jeu prend en charge un boîtier de jeu, vérifiez que le jeu reconnaît le contrôleur Xbox 360 pour Windows comme périphérique d’entrée \[ 1,4\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-540">RUNTIME 3: If the game supports a game pad, verify that the game recognizes Xbox 360 Controller for Windows as an input device \[1.4\]</span></span>

    1.  <span data-ttu-id="1c8dd-541">Si nécessaire, activez le contrôleur via le menu options.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-541">If needed, enable the controller via the options menu</span></span>
    2.  <span data-ttu-id="1c8dd-542">Vérifier que le jeu fait référence aux boutons et aux déclencheurs de contrôleur à l’aide des noms Xbox 360</span><span class="sxs-lookup"><span data-stu-id="1c8dd-542">Verify that the game refers to the controller buttons and triggers using Xbox 360 names</span></span>
    3.  <span data-ttu-id="1c8dd-543">Vérifier que le jeu et le système de menus sont contrôlable avec le contrôleur Xbox 360 pour Windows</span><span class="sxs-lookup"><span data-stu-id="1c8dd-543">Verify that the game and menu system are controllable with the Xbox 360 Controller for Windows</span></span>
    4.  <span data-ttu-id="1c8dd-544">Vérifier que le contrôleur Xbox 360 pour Windows se comporte conformément aux normes acceptées</span><span class="sxs-lookup"><span data-stu-id="1c8dd-544">Verify that the Xbox 360 Controller for Windows behaves according to accepted standards</span></span>

4.  <span data-ttu-id="1c8dd-545">Définissez la vidéo sur \[ 1,5 \] :</span><span class="sxs-lookup"><span data-stu-id="1c8dd-545">Set the video to \[1.5\]:</span></span>

    1.  <span data-ttu-id="1c8dd-546">Vérifier que le jeu s’exécute à une résolution de 4:3 de proportions (800 600 ou 1024 768)</span><span class="sxs-lookup"><span data-stu-id="1c8dd-546">Verify that the game runs at a 4:3 Aspect Ratio resolution (800 600 or 1024 768)</span></span>
    2.  <span data-ttu-id="1c8dd-547">Vérifier que le jeu s’exécute à une résolution de proportions 16:9 (1280 720)</span><span class="sxs-lookup"><span data-stu-id="1c8dd-547">Verify that the game runs at a 16:9 Aspect Ratio resolution (1280 720)</span></span>
    3.  <span data-ttu-id="1c8dd-548">Vérifier que le jeu s’exécute à une résolution de proportions 16:10 (1680 1050, 800 480 ou 1152 720)</span><span class="sxs-lookup"><span data-stu-id="1c8dd-548">Verify that the game runs at a 16:10 Aspect Ratio resolution (1680 1050, 800 480, or 1152 720)</span></span>
    4.  <span data-ttu-id="1c8dd-549">Vérifier que le jeu demande à l’utilisateur quand une modification est apportée à la résolution</span><span class="sxs-lookup"><span data-stu-id="1c8dd-549">Verify that the game prompts the user when a change is made to the resolution</span></span>
    5.  <span data-ttu-id="1c8dd-550">Vérifiez que l’affichage revient au paramètre précédent si vous n’acceptez pas dans les 15 secondes.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-550">Verify that the display reverts to the previous setting if you do not accept within 15 seconds</span></span>
    6.  <span data-ttu-id="1c8dd-551">Vérifier que le jeu n’étire pas l’image et, à son tour, présente une zone de vue plus vaste</span><span class="sxs-lookup"><span data-stu-id="1c8dd-551">Verify that the game does not stretch the picture and in turn presents a wider area of view</span></span>
    7.  <span data-ttu-id="1c8dd-552">Vérifier que le jeu n’ajoute pas de barres noires à gauche et à droite de la zone de jeu</span><span class="sxs-lookup"><span data-stu-id="1c8dd-552">Verify that the game does not add black bars to the left and right of the game play area</span></span>

5.  <span data-ttu-id="1c8dd-553">S’il est disponible dans les paramètres vidéo, vérifiez que les options de rendu du jeu sont par défaut Direct3D \[ 1,7 \] ; sinon, passez à [tests automatisés](#58-automated-tests)</span><span class="sxs-lookup"><span data-stu-id="1c8dd-553">If available in the video settings, verify that the game render options default to Direct3D \[1.7\]; otherwise, proceed to [Automated Tests](#58-automated-tests)</span></span>
6.  <span data-ttu-id="1c8dd-554">Si vous y êtes invité ou si l’option est disponible, créez un profil utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-554">If prompted or if the option is available, create a user profile.</span></span> <span data-ttu-id="1c8dd-555">Vérifier que le jeu ne rencontre pas d’erreurs lors de l’utilisation de noms de fichiers longs \[ 2,7\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-555">Verify that the game does not encounter errors when using long file names \[2.7\]</span></span>
7.  <span data-ttu-id="1c8dd-556">Démarrez un nouveau jeu, créez un jeu et vérifiez que le jeu ne rencontre pas d’erreurs lors de la gestion des caractères de système de fichiers non pris en charge \[ 2,7\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-556">Start a new game, create a game save, and verify that the game does not encounter errors when handling unsupported file system characters \[2.7\]</span></span>
8.  <span data-ttu-id="1c8dd-557">Vérifiez que le jeu est correctement ALT + tabulations sur le bureau Windows \[ 2,6\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-557">Verify that the game properly ALT+TABs to the Windows desktop \[2.6\]</span></span>

    1.  <span data-ttu-id="1c8dd-558">Permuter les utilisateurs avec le jeu en cours d’exécution en cliquant sur Démarrer-> changer d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="1c8dd-558">Switch users with the game running by clicking Start -> Switch User</span></span>
    2.  <span data-ttu-id="1c8dd-559">Ouvrir une session en tant que Toby</span><span class="sxs-lookup"><span data-stu-id="1c8dd-559">Log on as Toby</span></span>
    3.  <span data-ttu-id="1c8dd-560">Vérifiez que le jeu démarre en tant qu’utilisateur Toby, tout en étant toujours en cours d’exécution en tant qu’utilisateur Jane \[ 2,6\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-560">Verify that the game launches as User Toby while still running as User Jane \[2.6\]</span></span>
    4.  <span data-ttu-id="1c8dd-561">Vérifier que le jeu ne rencontre pas d’erreurs pour l’utilisateur Toby ou l’utilisateur Jane pendant le processus de changement d’utilisateur \[ 2,6\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-561">Verify that the game does not encounter errors for User Toby or User Jane during User Switch process \[2.6\]</span></span>
    5.  <span data-ttu-id="1c8dd-562">Vérifiez que vous ne pouvez pas entendre l’audio de la session de jeu d’origine \[ 2,6\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-562">Verify that you cannot hear audio from the original game session \[2.6\]</span></span>
    6.  <span data-ttu-id="1c8dd-563">Quitter le jeu</span><span class="sxs-lookup"><span data-stu-id="1c8dd-563">Exit the game</span></span>
    7.  <span data-ttu-id="1c8dd-564">Fermer la session Toby</span><span class="sxs-lookup"><span data-stu-id="1c8dd-564">Log off Toby</span></span>
    8.  <span data-ttu-id="1c8dd-565">Revenir à l’utilisateur d’origine sur lequel le jeu est en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="1c8dd-565">Switch back to the original user where the game is running</span></span>
    9.  <span data-ttu-id="1c8dd-566">ALT + TAB de nouveau dans le jeu</span><span class="sxs-lookup"><span data-stu-id="1c8dd-566">ALT+TAB back into the game</span></span>

9.  <span data-ttu-id="1c8dd-567">Quitter le jeu</span><span class="sxs-lookup"><span data-stu-id="1c8dd-567">Exit the game</span></span>
10. <span data-ttu-id="1c8dd-568">Passer au [Runtime](#56-post-runtime)</span><span class="sxs-lookup"><span data-stu-id="1c8dd-568">Proceed to [Post-Runtime](#56-post-runtime)</span></span>

### <a name="56-post-runtime"></a><span data-ttu-id="1c8dd-569">5,6 après le Runtime</span><span class="sxs-lookup"><span data-stu-id="1c8dd-569">5.6 Post-Runtime</span></span>

1.  <span data-ttu-id="1c8dd-570">Vérifier que le jeu ne génère pas d’erreurs à la sortie \[ 4,3\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-570">Verify that the game does not generate errors on exit \[4.3\]</span></span>
2.  <span data-ttu-id="1c8dd-571">Vérifier que le jeu est installé dans Program Files \[ 3,3\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-571">Verify that the game installed to Program Files \[3.3\]</span></span>
3.  <span data-ttu-id="1c8dd-572">Passer aux [contrôles de contrôle parental](/windows)</span><span class="sxs-lookup"><span data-stu-id="1c8dd-572">Proceed to [Parental Controls](/windows)</span></span>

### <a name="57-parental-controls"></a><span data-ttu-id="1c8dd-573">5,7 contrôle parental</span><span class="sxs-lookup"><span data-stu-id="1c8dd-573">5.7 Parental Controls</span></span>

1.  <span data-ttu-id="1c8dd-574">Ouvrir le contrôle parental dans le panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="1c8dd-574">Open Parental Controls in Control Panel</span></span>
2.  <span data-ttu-id="1c8dd-575">Vérifiez que le jeu affiche une évaluation exacte du contrôle parental sous le titre du jeu dans le panneau de configuration du contrôle parental \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-575">Verify that the game displays accurate Parental Control Rating below the game title in Parental Controls Control Panel \[1.2\]</span></span>
3.  <span data-ttu-id="1c8dd-576">Consultez le cas \[ de Test 1,2 \] pour les tests suivants :</span><span class="sxs-lookup"><span data-stu-id="1c8dd-576">See Test Case \[1.2\] for the following tests:</span></span>

    1.  <span data-ttu-id="1c8dd-577">Après avoir défini le contrôle parental sur « on », vérifiez que le jeu s’exécute avec ces paramètres en tant qu’utilisateur Jane \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-577">After setting Parental Controls to "On", verify that the game runs with these settings as User Jane \[1.2\]</span></span>
    2.  <span data-ttu-id="1c8dd-578">Déconnectez-vous et ouvrez une session en tant que Toby</span><span class="sxs-lookup"><span data-stu-id="1c8dd-578">Log off and log on as Toby</span></span>
    3.  <span data-ttu-id="1c8dd-579">Vérifiez que le jeu s’exécute avec ces paramètres en tant qu’utilisateur Toby \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-579">Verify that the game runs with these settings as User Toby \[1.2\]</span></span>
    4.  <span data-ttu-id="1c8dd-580">Déconnectez-vous et ouvrez une session en tant que Jane</span><span class="sxs-lookup"><span data-stu-id="1c8dd-580">Log off and log on as Jane</span></span>
    5.  <span data-ttu-id="1c8dd-581">Dans la section contrôle parental, empêchez l’utilisateur Toby de voir les jeux un niveau ESRB supérieur et supérieur du jeu que vous venez d’installer.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-581">In the Parental Control section, block User Toby from seeing games one ESRB level up and higher from the game that you just installed</span></span>

        <span data-ttu-id="1c8dd-582">Exemple : si le jeu est évalué E, définissez-le de sorte que Toby ne puisse jouer que des jeux classés en C</span><span class="sxs-lookup"><span data-stu-id="1c8dd-582">Example: If the game is rated E, set it so Toby can only play games that are rated C</span></span>

    6.  <span data-ttu-id="1c8dd-583">Vérifiez que le jeu s’exécute avec ces paramètres en tant qu’utilisateur Jane \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-583">Verify that the game runs with these settings as User Jane \[1.2\]</span></span>
    7.  <span data-ttu-id="1c8dd-584">Fermer la session et ouvrir une session en tant qu’utilisateur Toby</span><span class="sxs-lookup"><span data-stu-id="1c8dd-584">Log off and log on as user Toby</span></span>
    8.  <span data-ttu-id="1c8dd-585">Vérifier que le jeu n’est pas lancé sur l’utilisateur Toby lorsque ESRB est bloqué par l’utilisateur Jane \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-585">Verify that the game does not launch on User Toby when ESRB is blocked by User Jane \[1.2\]</span></span>
    9.  <span data-ttu-id="1c8dd-586">Déconnectez-vous en tant qu’utilisateur Toby et reconnectez-vous en tant qu’utilisateur Jane</span><span class="sxs-lookup"><span data-stu-id="1c8dd-586">Log off as user Toby and back on as user Jane</span></span>
    10. <span data-ttu-id="1c8dd-587">En cas de modification précédente, restaurez les paramètres ESRB</span><span class="sxs-lookup"><span data-stu-id="1c8dd-587">If changed previously, restore the ESRB settings</span></span>
    11. <span data-ttu-id="1c8dd-588">S’il n’existe aucun paramètre ESRB, sélectionnez « bloquer ou autoriser des jeux spécifiques », puis sélectionnez le jeu par son nom.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-588">If there are no ESRB settings, then select "Block or Allow Specific Games" and select the game by name</span></span>
    12. <span data-ttu-id="1c8dd-589">Déconnectez-vous en tant que Jane et en tant que Toby</span><span class="sxs-lookup"><span data-stu-id="1c8dd-589">Log off as Jane and on as Toby</span></span>
    13. <span data-ttu-id="1c8dd-590">Vérifier que le jeu n’est pas lancé sur l’utilisateur Toby lorsque l’utilisateur ou le nom est bloqué par l’utilisateur Jane \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-590">Verify that the game does not launch on User Toby when EXE/Name is blocked by User Jane \[1.2\]</span></span>
    14. <span data-ttu-id="1c8dd-591">Déconnectez-vous en tant que Toby et revenez sous le titre Jane</span><span class="sxs-lookup"><span data-stu-id="1c8dd-591">Log off as Toby and back on as Jane</span></span>
    15. <span data-ttu-id="1c8dd-592">Pour Jane, ouvrez contrôles utilisateur-> restrictions d’application</span><span class="sxs-lookup"><span data-stu-id="1c8dd-592">As Jane, open User Controls -> Application Restrictions</span></span>
    16. <span data-ttu-id="1c8dd-593">Cliquez sur « Toby ne peut utiliser que les programmes que je peux autoriser », puis cliquez sur OK (c’est-à-dire n’autoriser aucun exe)</span><span class="sxs-lookup"><span data-stu-id="1c8dd-593">Click "Toby can only use the programs I allow", and then click OK (i.e. allow no exes)</span></span>
    17. <span data-ttu-id="1c8dd-594">Cliquez sur la case décocher tout, puis sur OK.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-594">Click the Uncheck All box, and then click OK</span></span>
    18. <span data-ttu-id="1c8dd-595">Accéder à l’utilisateur contrôle les \| contrôles des jeux et autoriser le jeu spécifique à utiliser l’évaluation de la ESRB</span><span class="sxs-lookup"><span data-stu-id="1c8dd-595">Go to User Controls \| Games Controls and allow the specific game using the ESRB rating</span></span>
    19. <span data-ttu-id="1c8dd-596">Déconnectez-vous en tant que Jane et connectez-vous en tant que Toby et essayez de jouer au jeu</span><span class="sxs-lookup"><span data-stu-id="1c8dd-596">Log off as Jane and log on as Toby and try to play the game</span></span>
    20. <span data-ttu-id="1c8dd-597">Vérifiez que le jeu n’est pas bloqué et que Toby peut le lire quand « n’autoriser aucun exe » est défini \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-597">Verify that the game is NOT blocked and that Toby can play it when "allow no exes" is set \[1.2\]</span></span>
    21. <span data-ttu-id="1c8dd-598">Déconnectez-vous en tant qu’utilisateur Toby et reconnectez-vous en tant qu’utilisateur Jane</span><span class="sxs-lookup"><span data-stu-id="1c8dd-598">Log off as user Toby and back on as user Jane</span></span>
    22. <span data-ttu-id="1c8dd-599">Accédez à contrôle parental dans le panneau de configuration et supprimez les restrictions</span><span class="sxs-lookup"><span data-stu-id="1c8dd-599">Go to Parental Controls in Control Panel and remove the restrictions</span></span>
    23. <span data-ttu-id="1c8dd-600">Vérifier que les deux utilisateurs peuvent maintenant jouer au jeu</span><span class="sxs-lookup"><span data-stu-id="1c8dd-600">Verify that both users can now play the game</span></span>

4.  <span data-ttu-id="1c8dd-601">Passer aux [tests automatisés](#58-automated-tests)</span><span class="sxs-lookup"><span data-stu-id="1c8dd-601">Proceed to [Automated Tests](#58-automated-tests)</span></span>

### <a name="58-automated-tests"></a><span data-ttu-id="1c8dd-602">5,8 tests automatisés</span><span class="sxs-lookup"><span data-stu-id="1c8dd-602">5.8 Automated Tests</span></span>

1.  <span data-ttu-id="1c8dd-603">Vérifiez que le jeu ne génère pas d’erreurs lorsqu’il est exécuté sous Application Verifier-consultez documentation de l’outil de test de personnalisation \[ 4,2\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-603">Verify that the game does not generate failures when run under Application Verifier - See Branding Test Tool Documentation \[4.2\]</span></span>
2.  <span data-ttu-id="1c8dd-604">Vérifiez que les fichiers exécutables du jeu contiennent des manifestes. consultez la documentation de l’outil de test de personnalisation \[ 2,1\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-604">Verify that the game executable files contain manifests - see Branding Test Tool Documentation \[2.1\]</span></span>
3.  <span data-ttu-id="1c8dd-605">Vérifiez que le manifeste de fichier exécutable du jeu requestedExecutionLevel est « asInvoker ». consultez la documentation de l’outil de test de personnalisation \[ 2,1\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-605">Verify that the game executable file manifest requestedExecutionLevel is "AsInvoker" - see Branding Test Tool Documentation \[2.1\]</span></span>
4.  <span data-ttu-id="1c8dd-606">Passer à d' [autres tests](#59-other-tests)</span><span class="sxs-lookup"><span data-stu-id="1c8dd-606">Proceed to [Other Tests](#59-other-tests)</span></span>

### <a name="59-other-tests"></a><span data-ttu-id="1c8dd-607">5,9 autres tests</span><span class="sxs-lookup"><span data-stu-id="1c8dd-607">5.9 Other Tests</span></span>

1.  <span data-ttu-id="1c8dd-608">Vérifiez que les fichiers exécutables du jeu contiennent une signature numérique \[ 2,3\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-608">Verify that the game executable files contain a digital signature \[2.3\]</span></span>
2.  <span data-ttu-id="1c8dd-609">Vérifier que le processus d’installation du jeu s’exécute normalement sur les éditions 64 bits de Windows Vista et/ou Windows 7 \[ 2,3\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-609">Verify that the game installation process runs normally on 64-bit editions of Windows Vista and/or Windows 7 \[2.3\]</span></span>
3.  <span data-ttu-id="1c8dd-610">Vérifiez que le jeu ne rencontre pas d’erreur en raison d’exécutables 16 bits sur les éditions 64 bits de Windows Vista et/ou Windows 7 \[ 2,3\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-610">Verify that the game does not encounter an error as a result of 16-bit executables on 64-bit editions of Windows Vista and/or Windows 7 \[2.3\]</span></span>
4.  <span data-ttu-id="1c8dd-611">Forcer l’application à se bloquer pendant le test et vérifier que le jeu affiche Rapport d’erreurs Windows correctement et collecte les données de panne \[ 4,3\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-611">Force the application to crash while testing, and verify that the game displays Windows Error Reporting properly and collects crash data \[4.3\]</span></span>
5.  <span data-ttu-id="1c8dd-612">Garantir des résumés de fichiers appropriés \[ 4,3\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-612">Ensure proper file summaries \[4.3\]</span></span>

    1.  <span data-ttu-id="1c8dd-613">Cliquez sur Démarrer-> un ordinateur</span><span class="sxs-lookup"><span data-stu-id="1c8dd-613">Click Start -> Computer</span></span>
    2.  <span data-ttu-id="1c8dd-614">Accédez au répertoire du jeu</span><span class="sxs-lookup"><span data-stu-id="1c8dd-614">Navigate to the game directory</span></span>
    3.  <span data-ttu-id="1c8dd-615">Dans la fenêtre de recherche, tapez \*.dll</span><span class="sxs-lookup"><span data-stu-id="1c8dd-615">In the search window, type \*.dll</span></span>
    4.  <span data-ttu-id="1c8dd-616">Pour chaque fichier : cliquez avec le bouton droit sur le fichier, puis cliquez sur Propriétés.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-616">For each file: Right-click the file and click Properties</span></span>

        -   <span data-ttu-id="1c8dd-617">Dans Windows XP : cliquez sur l’onglet version. Vérifiez que les champs nom du produit, nom de la société et version du fichier sont correctement remplis.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-617">In Windows XP: Click the Version tab. Verify that the Product Name, Company Name, and File Version fields are properly populated.</span></span> <span data-ttu-id="1c8dd-618">\[4.3\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-618">\[4.3\]</span></span>
        -   <span data-ttu-id="1c8dd-619">Dans Windows Vista et Windows 7 : cliquez sur l’onglet Détails. Vérifiez que les champs nom du produit et version du fichier sont correctement remplis.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-619">In Windows Vista and Windows 7: Click the Details tab. Verify that the Product name and File Version fields are properly populated.</span></span> <span data-ttu-id="1c8dd-620">Le nom de la société n’est pas visible dans la page de propriétés de Windows Vista ou Windows 7 \[ 4,3\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-620">Company Name is not visible in the Windows Vista or Windows 7 properties page \[4.3\]</span></span>

    5.  <span data-ttu-id="1c8dd-621">Répétez cette vérification pour les fichiers .exe</span><span class="sxs-lookup"><span data-stu-id="1c8dd-621">Repeat this check for .exe files</span></span>

6.  <span data-ttu-id="1c8dd-622">Lancez le jeu.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-622">Launch the game.</span></span>

    1.  <span data-ttu-id="1c8dd-623">Appuyez sur CTRL + ALT + SUPPR</span><span class="sxs-lookup"><span data-stu-id="1c8dd-623">Press CTRL+ALT+DEL</span></span>
    2.  <span data-ttu-id="1c8dd-624">Cliquez sur la flèche « Options d’arrêt »</span><span class="sxs-lookup"><span data-stu-id="1c8dd-624">Click the "Shutdown Options" arrow</span></span>
    3.  <span data-ttu-id="1c8dd-625">Cliquez sur redémarrer</span><span class="sxs-lookup"><span data-stu-id="1c8dd-625">Click Restart</span></span>
    4.  <span data-ttu-id="1c8dd-626">Vérifier que le jeu ne bloque pas l’arrêt \[ 3,1\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-626">Verify game does not block shutdown \[3.1\]</span></span>

7.  <span data-ttu-id="1c8dd-627">Continuer la [désinstallation](#510-uninstall)</span><span class="sxs-lookup"><span data-stu-id="1c8dd-627">Proceed to [Uninstall](#510-uninstall)</span></span>

### <a name="510-uninstall"></a><span data-ttu-id="1c8dd-628">désinstallation de 5,10</span><span class="sxs-lookup"><span data-stu-id="1c8dd-628">5.10 Uninstall</span></span>

-   <span data-ttu-id="1c8dd-629">Vérifiez que le processus de désinstallation du jeu supprime tous les fichiers de composants du système d’exploitation non redistribués installés et efface tous les paramètres \[ 3,1\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-629">Verify that the game uninstallation process removes all installed, non-redistributed operating system component files and clears all settings \[3.1\]</span></span>

    -   <span data-ttu-id="1c8dd-630">Vérifiez dans Windows Vista ou Windows 7 que le panneau de configuration est le seul moyen de supprimer le programme \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="1c8dd-630">Verify in Windows Vista or Windows 7 that Control Panel is the only way to remove the program \[1.1\]</span></span>

## <a name="test-tool-notes"></a><span data-ttu-id="1c8dd-631">Notes de l’outil de test</span><span class="sxs-lookup"><span data-stu-id="1c8dd-631">Test Tool Notes</span></span>

<span data-ttu-id="1c8dd-632">Voici quelques remarques pour chacun des outils de test répertoriés dans les spécifications de test ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-632">These are notes for each of the test tools listed in the above test requirements.</span></span>

### <a name="61-appverifier-40-or-higher"></a><span data-ttu-id="1c8dd-633">6,1 AppVerifier 4,0 (ou version ultérieure)</span><span class="sxs-lookup"><span data-stu-id="1c8dd-633">6.1 Appverifier 4.0 (or higher)</span></span>

<span data-ttu-id="1c8dd-634">**Cas de test : 2,5, 4,2**</span><span class="sxs-lookup"><span data-stu-id="1c8dd-634">**Test Case: 2.5, 4.2**</span></span>

> [!Note]  
> <span data-ttu-id="1c8dd-635">Certaines applications ne peuvent pas s’exécuter avec AppVerifier en cours d’exécution, en raison de la protection contre la copie.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-635">Some applications fail to run with AppVerifier running, because of copy protection.</span></span> <span data-ttu-id="1c8dd-636">Cela peut être résolu en exécutant avec une version non protégée de l’exécutable du jeu.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-636">This can be resolved by running with an unprotected release version of the game executable.</span></span>

 

1.  <span data-ttu-id="1c8dd-637">Installer AppVerifier 4,0 (ou version ultérieure) sur un ordinateur exécutant Windows XP</span><span class="sxs-lookup"><span data-stu-id="1c8dd-637">Install AppVerifier 4.0 (or higher) on a computer running Windows XP</span></span>
2.  <span data-ttu-id="1c8dd-638">Lancez AppVerifier et cliquez sur fichier-> ajouter une application</span><span class="sxs-lookup"><span data-stu-id="1c8dd-638">Launch AppVerifier and click File -> Add Application</span></span>
3.  <span data-ttu-id="1c8dd-639">Recherchez l’exécutable du jeu, sélectionnez-le, puis cliquez sur Ouvrir.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-639">Locate the game executable, select it and click Open</span></span>
4.  <span data-ttu-id="1c8dd-640">Dans la section « applications », sélectionnez l’exécutable du jeu</span><span class="sxs-lookup"><span data-stu-id="1c8dd-640">In the "Applications" section, select the game executable</span></span>
5.  <span data-ttu-id="1c8dd-641">Dans la section « principes de base », sélectionnez les tests suivants :</span><span class="sxs-lookup"><span data-stu-id="1c8dd-641">Select the following tests in the "Basics" section:</span></span>

    -   <span data-ttu-id="1c8dd-642">Poignées</span><span class="sxs-lookup"><span data-stu-id="1c8dd-642">Handles</span></span>
    -   <span data-ttu-id="1c8dd-643">Tas</span><span class="sxs-lookup"><span data-stu-id="1c8dd-643">Heaps</span></span>
    -   <span data-ttu-id="1c8dd-644">Verrous</span><span class="sxs-lookup"><span data-stu-id="1c8dd-644">Locks</span></span>
    -   <span data-ttu-id="1c8dd-645">Mémoire</span><span class="sxs-lookup"><span data-stu-id="1c8dd-645">Memory</span></span>
    -   <span data-ttu-id="1c8dd-646">TLS</span><span class="sxs-lookup"><span data-stu-id="1c8dd-646">TLS</span></span>

6.  <span data-ttu-id="1c8dd-647">Sélectionnez les tests suivants dans la section « divers » :</span><span class="sxs-lookup"><span data-stu-id="1c8dd-647">Select the following tests in the "Miscellaneous" section:</span></span>

    -   <span data-ttu-id="1c8dd-648">DangerousAPIs</span><span class="sxs-lookup"><span data-stu-id="1c8dd-648">DangerousAPIs</span></span>
    -   <span data-ttu-id="1c8dd-649">DirtyStacks</span><span class="sxs-lookup"><span data-stu-id="1c8dd-649">DirtyStacks</span></span>

7.  <span data-ttu-id="1c8dd-650">Vérifiez que tous les autres tests ne sont pas sélectionnés</span><span class="sxs-lookup"><span data-stu-id="1c8dd-650">Ensure all other tests are not selected</span></span>
8.  <span data-ttu-id="1c8dd-651">Lancer le jeu</span><span class="sxs-lookup"><span data-stu-id="1c8dd-651">Launch the game</span></span>
9.  <span data-ttu-id="1c8dd-652">Jouer au jeu</span><span class="sxs-lookup"><span data-stu-id="1c8dd-652">Play the game</span></span>
10. <span data-ttu-id="1c8dd-653">Fermer le jeu</span><span class="sxs-lookup"><span data-stu-id="1c8dd-653">Close the game</span></span>
11. <span data-ttu-id="1c8dd-654">Dans AppVerifier, sélectionnez Afficher-> les journaux</span><span class="sxs-lookup"><span data-stu-id="1c8dd-654">In AppVerifier select View -> Logs</span></span>
12. <span data-ttu-id="1c8dd-655">Dans la section « applications », sélectionnez le fichier d' .exe d’application.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-655">In the "Applications" section select the app .exe file</span></span>
13. <span data-ttu-id="1c8dd-656">Dans la section « journaux », sélectionnez le fichier journal et observez le nombre d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-656">In the "Logs" section, select the log file and observe the error count.</span></span> <span data-ttu-id="1c8dd-657">S’il n’y a pas d’erreurs, terminez les tests AppVerifier.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-657">If there are no errors, then end AppVerifier tests.</span></span> <span data-ttu-id="1c8dd-658">Si des erreurs se produisent, cliquez sur le bouton afficher.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-658">If there are errors, click the View button</span></span>
14. <span data-ttu-id="1c8dd-659">Rechercher le document (CTRL + F) comme gravité = "erreur</span><span class="sxs-lookup"><span data-stu-id="1c8dd-659">Search the document (CTRL+F) for Severity="Error</span></span>
15. <span data-ttu-id="1c8dd-660">Créer des bogues basés sur la partie NomCouche = de l’échec</span><span class="sxs-lookup"><span data-stu-id="1c8dd-660">Create bugs based on the LayerName= portion of the failure</span></span>

### <a name="62-manifest-test---mtexe"></a><span data-ttu-id="1c8dd-661">6,2 manifeste de test-mt.exe</span><span class="sxs-lookup"><span data-stu-id="1c8dd-661">6.2 Manifest Test - mt.exe</span></span>

<span data-ttu-id="1c8dd-662">**Cas de test : 1,8, 2,1**</span><span class="sxs-lookup"><span data-stu-id="1c8dd-662">**Test Case: 1.8, 2.1**</span></span>

<span data-ttu-id="1c8dd-663">Cet outil est exécuté à partir d’une invite de commandes à l’emplacement où se trouve MT.exe.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-663">This tool is run from a command prompt where MT.exe is located.</span></span>

<span data-ttu-id="1c8dd-664">Exemple :</span><span class="sxs-lookup"><span data-stu-id="1c8dd-664">Example:</span></span>

``` syntax
mt.exe -inputresource:"c:\yourdir\YourGame.exe";#1 -out:yourgame.manifest
```

1.  <span data-ttu-id="1c8dd-665">Cliquez sur Démarrer-> exécuter-> tapez cmd et cliquez sur le bouton OK</span><span class="sxs-lookup"><span data-stu-id="1c8dd-665">Click Start -> Run -> type cmd and click the OK button</span></span>
2.  <span data-ttu-id="1c8dd-666">Exécutez l’outil mt.exe pour générer un fichier. manifest pour chaque fichier .exe qui est installé avec le jeu.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-666">Run the mt.exe tool to generate a .manifest file for each .exe file that installs with the game</span></span>
3.  <span data-ttu-id="1c8dd-667">Ouvrir le fichier. manifest généré</span><span class="sxs-lookup"><span data-stu-id="1c8dd-667">Open the generated .manifest file</span></span>
4.  <span data-ttu-id="1c8dd-668">Vérifiez que chaque fichier .exe contient les éléments suivants (demandés :</span><span class="sxs-lookup"><span data-stu-id="1c8dd-668">Ensure that each .exe file contains the following (requested:</span></span>

    ``` syntax
    <description>Example Game Name</description>
    <trustInfo xmlns="urn:schemas-microsoft-com:asm.v2">
      <security>
        <requestedPrivileges>
          <requestedExecutionLevel level="asInvoker"></requestedExecutionLevel>
        </requestedPrivileges>
      </security>
    </trustInfo>
      <asmv3:windowsSettings xmlns=http://schemas.microsoft.com/SMI/2005/WindowsSettings>
        <dpiAware>true<dpiAware>
      </asmv3:windowsSettings>
    </asmv3:application>
    ```

> [!Note]  
> <span data-ttu-id="1c8dd-669">Le niveau d’exécution demandé doit être présent pour chaque fichier, et dpiAware doit être présent pour au moins le fichier exécutable du jeu.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-669">Requested execution level should be present for every file, and dpiAware should be present for at least the game s executable file.</span></span>

 

### <a name="63-thread-hijacker---threadhijackerexe"></a><span data-ttu-id="1c8dd-670">détourneur de thread 6,3-threadhijacker.exe</span><span class="sxs-lookup"><span data-stu-id="1c8dd-670">6.3 Thread Hijacker - threadhijacker.exe</span></span>

<span data-ttu-id="1c8dd-671">Cet outil est exécuté à partir d’une invite de commandes à l’emplacement où se trouve threadhijacker.exe.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-671">This tool is run from a command prompt where threadhijacker.exe is located.</span></span>

<span data-ttu-id="1c8dd-672">Exemple :</span><span class="sxs-lookup"><span data-stu-id="1c8dd-672">Example:</span></span>

``` syntax
threadhijacker.exe /process:str
```

<span data-ttu-id="1c8dd-673">Où str est le nom \_ de \_program.exe</span><span class="sxs-lookup"><span data-stu-id="1c8dd-673">Where str is the name\_of\_program.exe</span></span>

1.  <span data-ttu-id="1c8dd-674">Affichez le gestionnaire des tâches, cliquez sur l’onglet processus, puis recherchez le nom de l’exécutable du jeu.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-674">Bring up Task Manager, click the Processes tab, and locate the name of the game executable.</span></span>
2.  <span data-ttu-id="1c8dd-675">Ouvrir une invite de commandes en mode administrateur</span><span class="sxs-lookup"><span data-stu-id="1c8dd-675">Open a command prompt in Admin mode</span></span>
3.  <span data-ttu-id="1c8dd-676">Accédez au répertoire où threadhijacker.exe est</span><span class="sxs-lookup"><span data-stu-id="1c8dd-676">Navigate to the directory where threadhijacker.exe is</span></span>
4.  <span data-ttu-id="1c8dd-677">Type : **threadhijacker.exe/process :** Str, où str est le nom de l’exécutable que vous souhaitez atteindre.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-677">Type: **threadhijacker.exe /process:** str, where str is the name of the executable that you want to hit</span></span>

### <a name="64-microsoft-games-for-windows-test-tool"></a><span data-ttu-id="1c8dd-678">6,4 Microsoft Games for Windows Test Tool</span><span class="sxs-lookup"><span data-stu-id="1c8dd-678">6.4 Microsoft Games for Windows Test Tool</span></span>

<span data-ttu-id="1c8dd-679">Cet outil se trouve dans le kit de développement logiciel (SDK) DirectX.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-679">This tool is located in the DirectX SDK.</span></span> <span data-ttu-id="1c8dd-680">Une fois le kit de développement logiciel (SDK) installé sur un ordinateur, le programme d’installation de l’outil de test Games for Windows peut être placé sur l’ordinateur de test et installé.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-680">Once the SDK is installed on a computer, the installer for the Games for Windows Test Tool can be placed on the test computer and installed.</span></span>

<span data-ttu-id="1c8dd-681">Recherchez le programme d’installation de Microsoft Games for Windows Test Tool sur l’ordinateur de développement sur lequel le kit de développement logiciel DirectX est installé.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-681">Locate the Microsoft Games for Windows Test Tool installer on the development computer where the DirectX SDK is installed.</span></span> <span data-ttu-id="1c8dd-682">Par défaut, il est placé à l’emplacement suivant :</span><span class="sxs-lookup"><span data-stu-id="1c8dd-682">By default, it is placed in the following location:</span></span>

``` syntax
%SystemDrive%\Program Files (x86)\Microsoft DirectX SDK (Date)\Utilities\bin\x86\Microsoft Games for Windows Test Tools\
```

1.  <span data-ttu-id="1c8dd-683">Copiez le programme d’installation (MicrosoftGFWTestTool.msi/setup.exe) sur l’ordinateur de test.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-683">Copy the installer (MicrosoftGFWTestTool.msi / setup.exe) to the test computer.</span></span>
2.  <span data-ttu-id="1c8dd-684">Exécutez le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-684">Run the installer.</span></span>
3.  <span data-ttu-id="1c8dd-685">Lancez l’outil de test Microsoft Games for Windows.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-685">Launch the Microsoft Games for Windows Test Tool.</span></span>
4.  <span data-ttu-id="1c8dd-686">Dans le champ **liste de projets** , remplacez **créer un projet** par le nom de votre titre, puis cliquez sur **créer**.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-686">In the **Project List** field replace **Create New Project** with your title name and click **Create New**.</span></span>

    <span data-ttu-id="1c8dd-687">Attendez la fin de la ligne de base.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-687">Wait for the Baseline to complete.</span></span>

5.  <span data-ttu-id="1c8dd-688">Renseignez toutes les informations que vous pouvez avoir dans la section informations sur le **jeu** , puis cliquez sur **mettre à jour les informations de jeu**.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-688">Fill in any information that you may have in the **Game Information** section, and click **Update Game Information**.</span></span>
6.  <span data-ttu-id="1c8dd-689">Cliquez sur l’onglet **cas de test** .</span><span class="sxs-lookup"><span data-stu-id="1c8dd-689">Click on **Test Cases** tab.</span></span>
7.  <span data-ttu-id="1c8dd-690">En commençant par le haut, suivez les cas de test, en cliquant sur **réussite** ou **échec** , le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-690">Starting at the top, proceed through the test cases, clicking **Pass** or **Fail** as appropriate.</span></span>

    <span data-ttu-id="1c8dd-691">Pour plus d’informations sur l’inclusion d’un bogue dans le rapport, consultez « écriture d’un bogue », plus loin dans cette section.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-691">See "Writing a Bug", later in this section, for details on including a bug in the report.</span></span>

8.  <span data-ttu-id="1c8dd-692">Revenez à l’onglet **projets** après avoir consulté le rapport (en vérifiant les onglets **rapport** et **modification des bogues** ).</span><span class="sxs-lookup"><span data-stu-id="1c8dd-692">Return to the **Projects** tab after reviewing the report (by checking the **Report** and **Bug Edit** tabs).</span></span>
9.  <span data-ttu-id="1c8dd-693">Cliquez sur **compiler le rapport**.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-693">Click **Compile Report**.</span></span>

    <span data-ttu-id="1c8dd-694">Une fenêtre s’ouvre lorsque la compilation du rapport est terminée.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-694">A window will open when the report is finished compiling.</span></span> <span data-ttu-id="1c8dd-695">Vous trouverez ici un .ZIP noms de fichiers *nom_projet* \_report.zip.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-695">Here you will find a .ZIP file names *ProjectName*\_report.zip.</span></span> <span data-ttu-id="1c8dd-696">Ce fichier contient tous les journaux et résultats collectés pendant la réussite du test.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-696">This file contains all of the logs and results collected during the test pass.</span></span>

### <a name="writing-a-bug"></a><span data-ttu-id="1c8dd-697">Écriture d’un bogue</span><span class="sxs-lookup"><span data-stu-id="1c8dd-697">Writing a Bug</span></span>

<span data-ttu-id="1c8dd-698">Il existe deux façons d’écrire un rapport de bogue : vous pouvez parcourir les cas de test et cliquer sur **échec** lorsque le titre échoue à un cas de test, ou vous pouvez cliquer sur l’onglet **modifier un bogue** et ajouter manuellement un rapport de bogue.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-698">There are two ways to write a bug report: you can go through the test cases and click **Fail** when the title fails a test case, or you can click the **Bug Edit** tab and manually add a bug report.</span></span>

### <a name="clicking-fail-on-a-test-case"></a><span data-ttu-id="1c8dd-699">Cliquer sur échec dans un cas de test</span><span class="sxs-lookup"><span data-stu-id="1c8dd-699">Clicking Fail on a test case</span></span>

1.  <span data-ttu-id="1c8dd-700">Lorsque vous cliquez sur **échec** dans un cas de test, la liste déroulante **type de problème** est automatiquement définie sur le type de cas de test.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-700">When you click **Fail** on a test case, the **Issue Type** drop-down list will automatically be set to the test case type.</span></span>
2.  <span data-ttu-id="1c8dd-701">Ajoutez une courte description au champ **titre** qui décrit brièvement le problème.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-701">Add a short description to the **Title** field that briefly describes the issue.</span></span>
3.  <span data-ttu-id="1c8dd-702">Ajoutez une description détaillée du problème au champ **comportement observé** .</span><span class="sxs-lookup"><span data-stu-id="1c8dd-702">Add a detailed description of the issue to the **Observed Behavior** field.</span></span>
4.  <span data-ttu-id="1c8dd-703">Le cas échéant, ajoutez ce qui était attendu (par opposition à une description du problème) au champ **comportement attendu** .</span><span class="sxs-lookup"><span data-stu-id="1c8dd-703">As appropriate, add what was expected (as opposed to a description of the issue) to the **Expected Behavior** field.</span></span>
5.  <span data-ttu-id="1c8dd-704">Ajoutez une description détaillée de la façon de reproduire le problème dans le champ **reproduction-étapes** .</span><span class="sxs-lookup"><span data-stu-id="1c8dd-704">Add a detailed description of how to reproduce the issue to the **Repro-Steps** field.</span></span>
6.  <span data-ttu-id="1c8dd-705">Lorsque vous avez terminé, cliquez sur le bouton **Enregistrer** .</span><span class="sxs-lookup"><span data-stu-id="1c8dd-705">When done, click the **Save** button.</span></span>

### <a name="manually-adding-a-bug"></a><span data-ttu-id="1c8dd-706">Ajout manuel d’un bogue</span><span class="sxs-lookup"><span data-stu-id="1c8dd-706">Manually Adding a Bug</span></span>

<span data-ttu-id="1c8dd-707">Ce processus revient à cliquer sur **échec**, à l’exception de la liste déroulante de remplissage automatique.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-707">This process is the same as clicking **Fail**, with the exception of the auto-populated drop-down list.</span></span> <span data-ttu-id="1c8dd-708">Dans ce cas, sélectionnez le type d’échec TCR approprié ou sélectionnez un **\* \* problème \* \* non-TR** pour les bogues qui se trouvent en dehors de la plage TR mais qui doivent toujours être signalés.</span><span class="sxs-lookup"><span data-stu-id="1c8dd-708">In this case, either select the appropriate TCR failure type or select **\*\* Non-TR Issue \*\*** for bugs that fall outside of the TR range but should still be reported.</span></span>

## <a name="resources"></a><span data-ttu-id="1c8dd-709">Ressources</span><span class="sxs-lookup"><span data-stu-id="1c8dd-709">Resources</span></span>

<dl> <dt>

<span data-ttu-id="1c8dd-710"><span id="Games_for_Windows__Technical_Requirements"></span><span id="games_for_windows__technical_requirements"></span><span id="GAMES_FOR_WINDOWS__TECHNICAL_REQUIREMENTS"></span>Jeux pour Windows : exigences techniques</span><span class="sxs-lookup"><span data-stu-id="1c8dd-710"><span id="Games_for_Windows__Technical_Requirements"></span><span id="games_for_windows__technical_requirements"></span><span id="GAMES_FOR_WINDOWS__TECHNICAL_REQUIREMENTS"></span>Games for Windows: Technical Requirements</span></span>
</dt> <dd>

[<span data-ttu-id="1c8dd-711">Jeux pour les exigences techniques de Windows : meilleures pratiques pour les jeux sur Windows XP, Windows Vista et Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c8dd-711">Games for Windows Technical Requirements: Best Practices for Games on Windows XP, Windows Vista, and Windows 7</span></span>](./games-for-windows-technical-requirements-1-1-0006.md)

</dd> <dt>

<span data-ttu-id="1c8dd-712"><span id="Windows_SDK"></span><span id="windows_sdk"></span><span id="WINDOWS_SDK"></span>SDK Windows</span><span class="sxs-lookup"><span data-stu-id="1c8dd-712"><span id="Windows_SDK"></span><span id="windows_sdk"></span><span id="WINDOWS_SDK"></span>Windows SDK</span></span>
</dt> <dd>

[<span data-ttu-id="1c8dd-713">Kits de développement logiciel Windows</span><span class="sxs-lookup"><span data-stu-id="1c8dd-713">Windows SDKs</span></span>](https://msdn.microsoft.com/bb980924.aspx)

</dd> <dt>

<span data-ttu-id="1c8dd-714"><span id="User_Account_Control_Guidelines"></span><span id="user_account_control_guidelines"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES"></span>Instructions relatives au contrôle de compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="1c8dd-714"><span id="User_Account_Control_Guidelines"></span><span id="user_account_control_guidelines"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES"></span>User Account Control Guidelines</span></span>
</dt> <dd>

<span data-ttu-id="1c8dd-715">[Exigences de développement d’applications Windows Vista pour la compatibilité du contrôle de compte d’utilisateur](/previous-versions/dotnet/articles/bb530410(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="1c8dd-715">[Windows Vista Application Development Requirements for User Account Control Compatibility](/previous-versions/dotnet/articles/bb530410(v=msdn.10))</span></span>

</dd> <dt>

<span data-ttu-id="1c8dd-716"><span id="Windows_Installer_Information"></span><span id="windows_installer_information"></span><span id="WINDOWS_INSTALLER_INFORMATION"></span>Informations Windows Installer</span><span class="sxs-lookup"><span data-stu-id="1c8dd-716"><span id="Windows_Installer_Information"></span><span id="windows_installer_information"></span><span id="WINDOWS_INSTALLER_INFORMATION"></span>Windows Installer Information</span></span>
</dt> <dd>

[<span data-ttu-id="1c8dd-717">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="1c8dd-717">Windows Installer</span></span>](../msi/windows-installer-portal.md)

</dd> <dt>

<span data-ttu-id="1c8dd-718"><span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>Portail des développeurs WinQual</span><span class="sxs-lookup"><span data-stu-id="1c8dd-718"><span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>WinQual Developer Portal</span></span> 
</dt> <dd>

[<span data-ttu-id="1c8dd-719">Windows Quality Online Services (winqual)</span><span class="sxs-lookup"><span data-stu-id="1c8dd-719">Windows Quality Online Services (Winqual)</span></span>](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)

</dd> <dt>

<span data-ttu-id="1c8dd-720"><span id="DirectX_Developer_Portal"></span><span id="directx_developer_portal"></span><span id="DIRECTX_DEVELOPER_PORTAL"></span>Portail des développeurs DirectX</span><span class="sxs-lookup"><span data-stu-id="1c8dd-720"><span id="DirectX_Developer_Portal"></span><span id="directx_developer_portal"></span><span id="DIRECTX_DEVELOPER_PORTAL"></span>DirectX Developer Portal</span></span>
</dt> <dd>

<span data-ttu-id="1c8dd-721">[Centre de développement DirectX](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="1c8dd-721">[DirectX Developer Center](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>

</dd> <dt>

<span data-ttu-id="1c8dd-722"><span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Blog sur les jeux pour Windows et DirectX SDK</span><span class="sxs-lookup"><span data-stu-id="1c8dd-722"><span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Games for Windows and DirectX SDK Blog</span></span>
</dt> <dd>

[<span data-ttu-id="1c8dd-723">Jeux pour Windows et kit de développement logiciel (SDK) DirectX</span><span class="sxs-lookup"><span data-stu-id="1c8dd-723">Games for Windows and the DirectX SDK</span></span>](https://walbourn.github.io/)

</dd> <dt>

<span data-ttu-id="1c8dd-724"><span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Autres articles DirectX</span><span class="sxs-lookup"><span data-stu-id="1c8dd-724"><span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Additional DirectX Articles</span></span>
</dt> <dd>

[<span data-ttu-id="1c8dd-725">Articles techniques sur DirectX</span><span class="sxs-lookup"><span data-stu-id="1c8dd-725">DirectX Technical Articles</span></span>](./dx9-technical-articles.md)

</dd> </dl>

 

