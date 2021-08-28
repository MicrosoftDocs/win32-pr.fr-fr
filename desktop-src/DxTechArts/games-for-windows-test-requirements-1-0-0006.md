---
title: 'Cas de test des jeux pour Windows : bonnes pratiques pour les jeux sur Windows XP, Windows Vista, Windows 7 et Windows 8'
description: Cet article fournit des cas de test pour les jeux pour Windows.
ms.assetid: bbe84d3f-e7ff-f14f-ec25-ae1c980749fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aeda677a32d73ccb305eb350b9c4c1231bb0bf4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886429"
---
# <a name="games-for-windows-test-cases-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8"></a>jeux pour Windows cas de Test : meilleures pratiques pour les jeux sur Windows XP, Windows Vista, Windows 7 et Windows 8

Cet article fournit des cas de test pour les jeux pour Windows.

## <a name="how-to-use-this-article"></a>Procédure d'utilisation de cet article

Cet article comporte trois sections principales :

<dl> <dt>

<span id="Test_Requirements"></span><span id="test_requirements"></span><span id="TEST_REQUIREMENTS"></span>**Spécifications de test**
</dt> <dd>

Chaque spécification de test dans ce document comporte quatre sections principales : un titre et une table avec trois sections notables (colonne de gauche, droite en haut, à droite en bas).

<dl> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>Bonhomme
</dt> <dd>

Nom du cas de test.

</dd> <dt>

<span id="Box__far_left_column"></span><span id="box__far_left_column"></span><span id="BOX__FAR_LEFT_COLUMN"></span>Box, colonne de gauche
</dt> <dd>

Noms des systèmes d’exploitation auxquels s’applique le cas de test.

</dd> <dt>

<span id="Box__right_top"></span><span id="box__right_top"></span><span id="BOX__RIGHT_TOP"></span>Box, à droite en haut
</dt> <dd>

Bref résumé du cas de test.

</dd> <dt>

<span id="Box__right_bottom"></span><span id="box__right_bottom"></span><span id="BOX__RIGHT_BOTTOM"></span>Box, à droite en bas
</dt> <dd>

Détails du cas de test réel.

</dd> </dl> </dd> <dt>

<span id="Sample_Test_Script"></span><span id="sample_test_script"></span><span id="SAMPLE_TEST_SCRIPT"></span>**Exemple de script de test**
</dt> <dd>

Cette section est un exemple de la séquence qu’une passe de test typique suivra si vous utilisez les spécifications de test comme guide.

</dd> <dt>

<span id="Test_Tool_Notes"></span><span id="test_tool_notes"></span><span id="TEST_TOOL_NOTES"></span>**Notes de l’outil de test**
</dt> <dd>

Cette section contient des remarques détaillées sur chacun des outils de test utilisés pour vérifier les conditions de réussite ou d’échec dans les spécifications de test.

</dd> </dl>

## <a name="test-requirements"></a>Spécifications de test

### <a name="1-game-requirements"></a>1. spécifications du jeu

### <a name="11-windows-games-explorer"></a>1,1 Windows l’explorateur de jeux



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>le jeu doit être visible dans l’explorateur de jeux sur Windows Vista et Windows 7. Lorsque cette option est sélectionnée, le jeu doit également afficher les métadonnées correctes. l’installation ne doit pas créer de raccourci pour lancer le jeu sur le bureau, dans le menu Démarrer ou dans un autre emplacement. Les tâches et les raccourcis de suppression ne doivent pas être créés.</td>
</tr>
<tr class="even">

<td><ol>
<li>Après avoir installé le jeu, ouvrez l’Explorateur de jeux.</li>
<li>Vérifiez que l’icône de jeu s’affiche dans l’Explorateur de jeux.</li>
<li>Cliquez avec le bouton droit sur l’icône et testez chaque tâche de support de lecture & définie par l’application.</li>
<li>Cliquez sur l’icône et vérifiez que les métadonnées (éditeur, développeur, genre, date de publication, version) s’affichent en bas et sont correctes.</li>
<li>vérifiez que l’icône du jeu Windows affiche des informations sur l’WEI d’expérience utilisateur dans l’explorateur de jeux.</li>
<li>Vérifiez que les liens hypertexte de jeu pour les métadonnées fonctionnent correctement dans l’Explorateur de jeux. (Si les liens hypertexte ne s’affichent pas, il s’agit d’un signe possible que l’exe n’est pas signé ; consultez la <a href="#23-sign-files">section 2,3</a>.)</li>
<li>Vérifiez que le jeu affiche une évaluation précise du contrôle parental dans l’Explorateur de jeux. (S’il indique non évalué, vérifiez qu’il s’agit d’un jeu non classé ; sinon, il s’agit d’un indicateur que l’exe n’est pas signé ; consultez la <a href="#23-sign-files">section 2,3</a>.)</li>
<li>Vérifiez que le jeu ne place pas de raccourcis de lancement sur le Bureau de l’utilisateur.</li>
<li>Cliquez sur Démarrer-> tous les programmes.</li>
<li>Vérifiez que le jeu ne place pas de raccourcis de lancement dans le menu Démarrer.</li>
<li>Vérifiez que le jeu ne place pas les raccourcis de désinstallation dans le menu démarrer en dehors du panneau de configuration.</li>
<li>si le jeu est distribué numériquement, vérifiez que le fournisseur de services s’affiche dans Windows l’explorateur de jeux.</li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="12-windows-family-safety--parental-controls"></a>contrôle parental/sécurité de la famille 1,2 Windows



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>Le jeu doit s’exécuter dans le contexte d’un &quot; utilisateur standard &quot; . Le contrôle parental doit pouvoir bloquer le jeu. Vérifiez que le fichier GDF contient des noms EXE.</td>
</tr>
<tr class="even">

<td><ol>
<li>créez un compte d’utilisateur Standard dans Windows Vista ou Windows 7 appelé Toby. Démarrer-> le panneau de configuration-> ajouter ou supprimer des comptes d’utilisateur-> créer un nouveau compte</li>
<li>En tant que Jane, à partir du compte administrateur, configurez les contrôles parentaux pour le jeu. Démarrer-> panneau de configuration-> configurer des contrôles parentaux pour les Toby d’un utilisateur >
<ol>
<li>Vérifiez que le jeu est lancé à partir de l’icône Explorateur de jeux.</li>
<li>Vérifiez que le jeu affiche une évaluation exacte du contrôle parental sous le titre du jeu dans le panneau de configuration du contrôle parental.</li>
<li>Avant d’appliquer les contrôles parentaux, vérifiez que le jeu ne demande pas d’informations d’identification d’administrateur au lancement.</li>
<li>Définissez contrôle parental &quot; sur activé &quot; .</li>
<li>dans la section Paramètres Windows, cliquez sur jeux.</li>
<li>Cliquez sur OK (le paramètre doit maintenant être &quot; AO/All Games &quot; ).</li>
<li>Vérifiez que le jeu s’exécute avec ces paramètres en tant qu’utilisateur Jane.</li>
<li>Déconnectez-vous en tant que Jane et connectez-vous en tant que Toby.</li>
<li>Vérifiez que le jeu s’exécute avec ces paramètres en tant qu’utilisateur Toby.</li>
<li>Déconnectez-vous en tant que Toby et connectez-vous en tant que Jane.</li>
<li>Revenez à l’écran précédent et sélectionnez &quot; définir les évaluations de jeux &quot; .</li>
<li><p>Sélectionnez une évaluation inférieure à l’évaluation de la ESRB du jeu.</p>
<blockquote>
[!Note]<br />
Si le jeu n’est pas évalué, ignorez cette étape et passez à la partie suivante de ce test. Il peut être nécessaire de choisir un système d’évaluation différent pour trouver une évaluation du jeu, en fonction des paramètres régionaux de langue de la référence SKU testée.
</blockquote>
<p><br/></p></li>
<li>Déconnectez-vous en tant que Jane et connectez-vous en tant que Toby.</li>
<li>Vérifiez que le jeu n’est pas lancé pour l’utilisateur Toby lorsque ESRB est bloqué par l’utilisateur Jane.</li>
<li>Déconnectez-vous en tant que Toby et connectez-vous en tant que Jane.</li>
<li>En cas de modification précédente, restaurez les paramètres ESRB.</li>
<li>S’il n’existe aucun paramètre ESRB, sélectionnez &quot; bloquer ou autoriser des jeux spécifiques, &quot; puis sélectionnez le jeu par son nom.</li>
<li>Déconnectez-vous en tant que Jane et connectez-vous en tant que Toby.</li>
<li>Vérifiez que le jeu n’est pas lancé pour l’utilisateur Toby lorsque l’utilisateur ou le nom est bloqué par l’utilisateur Jane.</li>
<li>Déconnectez-vous en tant que Toby et revenez sous le titre Jane.</li>
<li>Pour Jane, ouvrez contrôles utilisateur-> restrictions d’application.</li>
<li>Cliquez sur &quot; Toby ne peut utiliser que les programmes que j’autorise &quot; , puis cliquez sur OK (autrement dit, n’autoriser aucun exe).</li>
<li>Accéder aux contrôles utilisateur | Les jeux contrôlent et permettent le jeu spécifique à l’aide de l’évaluation ESRB.</li>
<li>Déconnectez-vous en tant que Jane et connectez-vous en tant que Toby et essayez de jouer au jeu.</li>
<li>Vérifiez que le jeu n’est pas bloqué et que Toby peut le lire quand &quot; aucun exe &quot; n’est défini.</li>
</ol></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="13-windows-vista-rich-saved-games"></a>1,3 jeux enrichis Windows Vista

Cette exigence a été supprimée.

### <a name="14-xbox-360-common-controller-for-windows-conditional-requirement"></a>1,4 Xbox 360 contrôleur commun pour Windows \[ exigence conditionnelle\]



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>les jeux qui prennent en charge les contrôleurs de manette doivent prendre en charge le manette Xbox 360 pour Windows à l’aide de l’API XInput. Toutes les références aux déclencheurs et aux boutons du contrôleur commun doivent utiliser les noms Xbox 360.</td>
</tr>
<tr class="even">

<td><ol>
<li>Lancez le jeu.</li>
<li>Accédez aux options du contrôleur. **</li>
<li>vérifiez que le jeu reconnaît manette Xbox 360 pour Windows en tant qu’appareil d’entrée.</li>
<li>jouez au jeu et vérifiez que le jeu et le système de menus sont contrôlable avec manette Xbox 360 pour Windows.</li>
<li>vérifiez que le manette Xbox 360 pour Windows se comporte conformément aux normes acceptées. (B pour précédent, A pour accepter, démarrer pour dans le menu jeu/suspendre ou accepter, etc.)</li>
<li>Vérifiez que le jeu fait référence aux boutons et aux déclencheurs de contrôleur à l’aide des noms Xbox 360.</li>
</ol>
<br/>
<blockquote>
[!Note]<br />
Si le jeu ne prend pas en charge un contrôleur de jeu et/ou ne prend en charge que le clavier/la souris, ignorez ce cas de test.
</blockquote>
<br/> * * Paramètres pour le contrôleur peut être situé en dehors du jeu. <br/></td>
</tr>
</tbody>
</table>



 

### <a name="15-multiple-aspect-ratios-and-resolutions"></a>1,5 plusieurs proportions et résolutions



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Le jeu doit prendre en charge au moins les proportions et les résolutions d’écran associées suivantes : <br/>
<ul>
<li>4:3 &quot; normal &quot; (800 600 ou 1024 768)</li>
<li>&quot;écran large 16:9 &quot; (1280 720)</li>
<li>16:10 &quot; grand écran &quot; (1152 720, 1680 1050 ou 800 480)</li>
</ul></td>
</tr>
<tr class="even">

<td>Recherchez les options vidéo pour le jeu (cela peut être dans notre jeu).<br/>
<blockquote>
[!Note]<br />
Les tests suivants doivent être effectués sur une analyse panoramique.
</blockquote>
<br/>
<ol>
<li>Dans la section résolution vidéo, sélectionnez 800 600 ou 1024 768.</li>
<li>Vérifiez que le jeu s’exécute avec une résolution de proportions de 4:3.</li>
<li>Dans la section résolution vidéo, sélectionnez 1280 720.</li>
<li>Vérifiez que le jeu s’exécute avec une résolution de proportions de 16:9.</li>
<li>Dans la section résolution vidéo, sélectionnez 1680 1050, 800 480 ou 1152 720.</li>
<li>Vérifiez que le jeu s’exécute avec une résolution de proportions de 16:10.</li>
<li>Vérifiez que le jeu n’étire pas l’image et, à son tour, présente une zone de vue plus vaste.</li>
<li>Vérifiez que le jeu demande à l’utilisateur quand une modification est apportée à la résolution.</li>
<li>Si l’utilisateur n’accepte pas dans les 15 secondes, vérifiez que l’affichage est rétabli sur le paramètre précédent.</li>
<li>Vérifiez que le jeu n’ajoute pas de barres noires à gauche et à droite de la zone de jeu. (Dans ce cas, la zone de jeu se trouve toujours dans un ratio 4:3 au milieu de l’écran.)</li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="16-windows-media-center"></a>1,6 Windows Media Center

Cette exigence a été supprimée.

### <a name="17-direct3d-conditional-requirement"></a>1,7 \[ condition conditionnelle Direct3D\]



| Système d''exploitation                                                                    | Condition requise                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows 7<br/> Windows Vista<br/> Windows XP<br/> | Si le jeu utilise Direct3D, la version minimale prise en charge doit être Direct3D 9, et Direct3D doit être la valeur par défaut pour toutes les options de configuration de l’affichage.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|     <dl> <dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manuel</dt> <dd> Lancez le jeu. Dans les options vidéo, vérifiez s’il existe des options de rendu, D3D et/ou OpenGL. Si c’est le cas, vérifiez que les options de rendu du jeu sont par défaut Direct3D. Si vous ne parvenez pas à vérifier que D3D9 est la version de DirectX en cours d’utilisation, passez au test automatisé. <br/> </dd> <dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Test automatisé</dt> <dd> Utiliser l’outil : Depends.exe <br/> </dd> </dl> |



 

### <a name="18-enable-high-dpi-aware"></a>1,8 activer la prise en charge des résolutions élevées



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>Les jeux et leurs programmes d’installation doivent s’exécuter correctement sans problèmes visuels lorsque la mise à l’échelle DPI est activée.</td>
</tr>
<tr class="even">

<td><dl> <dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manuelle</dt> <dd>
<ol>
<li>Définissez le système sur PPP 150% : <br/> Windows Vista : panneau de configuration : personnalisation, ajuster la taille de police (DPI), résolution personnalisée. Définissez sur 150%.<br/> Windows 7 : panneau de configuration : affichage, défini sur plus de 150%.<br/></li>
<li>Exécutez le processus et le jeu d’installation pour vérifier qu’il n’y a aucun problème avec les écrans détourés ou les boîtes de dialogue.</li>
</ol>
</dd> <dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Test automatisé</dt> <dd> Vérifiez que &lt; l’élément dpiAware &gt; true </dpiAware> est contenu dans le manifeste incorporé.<br/> Utiliser l’outil : Mt.exe <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="2-security-and-compatibility"></a>2. sécurité et compatibilité

### <a name="21-follow-user-account-control-guidelines"></a>2,1 suivre les instructions relatives au contrôle de compte d’utilisateur



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>Chaque fichier exécutable (extension .EXE) inclus dans une application doit avoir un manifeste incorporé qui définit son niveau d’exécution :
<pre class="syntax" data-space="preserve"><code><requestedExecutionLevel level=&quot;asInvoker|highestAvailable|requireAdministrator&quot; 
              uiAccess=&quot;true|false&quot;/></code></pre>
<br/>
<blockquote>
[!Note]<br />
Pour les jeux et les programmes d’installation de jeu, uiAccess doit toujours avoir la valeur &quot; false &quot; .
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td><ol>
<li>Vérifiez que les fichiers exécutables de jeu contiennent des manifestes.</li>
<li>Vérifiez que le manifeste de fichier exécutable du jeu requestedExecutionLevel est &quot; asInvoker &quot; .</li>
</ol>
Utiliser l’outil : Mt.exe <br/></td>
</tr>
</tbody>
</table>



 

### <a name="22-support-x64-versions-of-windows"></a>2,2 prendre en charge les versions x64 de Windows



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>Pour maintenir la compatibilité avec les versions x64 de Windows : <br/>
<ul>
<li>Les programmes d’installation de titres et de titres ne doivent pas contenir de code 16 bits ou ne s’appuient sur aucun composant 16 bits.</li>
<li>Si le jeu dépend des pilotes en mode noyau pour fonctionner, les versions x64 de ces pilotes doivent être disponibles. Le programme d’installation du jeu doit détecter et installer les pilotes et les composants appropriés pour les éditions 64 bits de Windows.</li>
</ul>
<blockquote>
[!Note]<br />
la prise en charge de l’édition 64 bits de Windows XP Professional est facultative.
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td>Test manuel<br/>
<ol>
<li>Exécutez le jeu sur les éditions 64 bits de Windows. vérifiez que le processus d’installation du jeu s’exécute normalement sur les éditions 64 bits de Windows Vista ou Windows 7.</li>
<li>vérifiez que le jeu ne rencontre pas d’erreur en raison d’exécutables 16 bits sur les éditions 64 bits de Windows Vista ou Windows 7. L’erreur indiquera l’application 16 bits dans la fenêtre d’erreur.</li>
<li>Si le jeu est doté d’un exécutable 64 bits natif, utilisez-le également.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="23-sign-files"></a>2,3 fichiers de signature



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Tous les fichiers de code exécutable (par exemple, les extensions .exe et .dll) doivent être signés avec un certificat Authenticode. <br/> si vous utilisez Windows Installer, les fichiers de package du programme d’installation (fichiers .msi) doivent être signés. <br/></td>
</tr>
<tr class="even">

<td>Test manuel<br/>
<ol>
<li>Accédez au répertoire du jeu.</li>
<li>Recherchez tous les fichiers .exe et .dll.</li>
<li>Cliquez avec le bouton droit sur Propriétés dans chaque fichier.</li>
<li>Vérifiez que les fichiers exécutables du jeu contiennent une signature numérique.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="24-sign-drivers"></a>2,4 signer les pilotes



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Tout pilote en mode noyau installé par le jeu doit être signé avec un certificat Authenticode publiquement valide. <br/> tout pilote de périphérique en mode noyau installé par le jeu doit avoir une signature Microsoft obtenue par le biais du programme Windows WHQL (hardware Quality Labs) ou DRS (driver fiabilite signature). <br/></td>
</tr>
<tr class="even">

<td>Test manuel<br/>
<ol>
<li>Installez le jeu.</li>
<li>Vérifiez que le processus d’installation du jeu n’affiche pas de boîte (s) de dialogue de pilote non signé.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="25-perform-version-checking-properly"></a>2,5 effectuer la vérification de la version correctement



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>les jeux ne doivent pas être exécutés sur des systèmes d’exploitation ultérieurs, comme indiqué par les modifications apportées au numéro de version Windows, sauf si le contrat de licence utilisateur final interdit l’utilisation sur les systèmes d’exploitation ultérieurs. Si le jeu est supposé échouer, il doit le faire normalement en affichant un message à l’utilisateur.</td>
</tr>
<tr class="even">

<td><dl> <dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manuelle</dt> <dd>
<ol>
<li>installez le jeu sur Windows XP, sur les éditions 32 bits de Windows vista et Windows 7, ainsi que sur les éditions 64 bits de Windows vista et Windows 7.</li>
<li>Vérifiez que le processus d’installation du jeu ne rencontre pas d’erreur concernant la version du système d’exploitation.</li>
</ol>
</dd> <dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Test automatisé</dt> <dd> Utiliser l’outil : Application Verifier<br/>
<ol>
<li>Lancez Application Verifier.</li>
<li>Activez le test de compatibilité : HighVersionLie après avoir sélectionné l' INSTALL.EXE.</li>
<li>Installez le jeu et assurez-vous qu’il ne bloque pas l’installation en fonction de la version du système d’exploitation.</li>
<li>Activez le test de compatibilité : HighVersionLie après avoir sélectionné l' GAME.EXE.</li>
<li>Exécutez le jeu et assurez-vous qu’il ne bloque pas l’exécution en fonction de la version du système d’exploitation.</li>
</ol>
</dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="26-support-concurrent-user-sessions"></a>2,6 prendre en charge les sessions utilisateur simultanées



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>les jeux doivent prendre en charge les scénarios de multitâches Windows standard.</td>
</tr>
<tr class="even">

<td>créez un compte d’utilisateur Standard dans Windows Vista ou Windows 7 appelé Toby. Démarrer-> le panneau de configuration-> ajouter ou supprimer des comptes d’utilisateur-> créer un nouveau compte <br/>
<ol>
<li>Lancez le jeu en tant qu’utilisateur Jane.</li>
<li>ALT + TAB de nouveau sur le bureau.</li>
<li>vérifiez que le jeu est correctement ALT + tabulations sur le bureau de Windows.</li>
<li>Cliquez sur Start-> [flèche à droite de LOCK]-> changer d’utilisateur.</li>
<li>Ouvrez une session en tant qu’utilisateur Toby.</li>
<li>Vérifiez que le jeu démarre en tant qu’utilisateur Toby, tout en étant toujours en cours d’exécution en tant qu’utilisateur Jane.</li>
<li>Vérifiez que le jeu ne rencontre pas d’erreurs pour l’utilisateur Toby ou l’utilisateur Jane pendant le processus de changement d’utilisateur.</li>
<li>Si vous pouvez lancer une autre session de jeu, vérifiez que vous ne pouvez pas entendre l’audio de la session de jeu d’origine.</li>
<li>Fermez le jeu et revenez à l’utilisateur et au jeu d’origine.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="27-support-long-names"></a>2,7 prendre en charge les noms longs



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Si un jeu prend en charge l’enregistrement de fichiers, il doit être en mesure d’enregistrer des fichiers avec des noms et des chemins d’accès longs. Le jeu doit gérer correctement les caractères spéciaux du système de fichiers, tels que \/ : * ? &quot; < ou > dans les champs d’entrée utilisateur utilisés pour créer des noms de fichiers ou des chemins d’accès.</td>
</tr>
<tr class="even">

<td><ol>
<li>Lancez le jeu.</li>
<li>Démarrez un nouveau jeu.</li>
<li>Enregistrez le jeu. Pendant le processus d’enregistrement, vérifiez que le jeu enregistre à l’aide de la première partie enregistrer le nom : My First Save.</li>
<li>Revenez au menu principal.</li>
<li>Essayez de charger le jeu qui vient d’être enregistré.</li>
<li>Vérifier que le jeu ne rencontre pas d’erreurs lors de la gestion des caractères de système de fichiers non pris en charge, tels que \/ : * ? &quot; < ou > si le jeu vous permet de nommer le jeu enregistré.</li>
<li>Si l’utilisateur est autorisé à nommer son profil et/ou son caractère ou à enregistrer des parties, vérifiez que le jeu ne rencontre pas d’erreurs lors de l’utilisation de noms de fichiers longs ici également.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="3-installation"></a>3. installation

### <a name="31-easy-install"></a>Installation facile de 3,1



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Les jeux avec une installation traditionnelle doivent fournir un chemin d’accès simplifié dans leur interface utilisateur d’installation.</td>
</tr>
<tr class="even">

<td><ol>
<li>Insérez le disque du jeu.</li>
<li>Vérifiez que le jeu n’affiche pas plus d’un contrat de licence End-User (CLUF).</li>
<li>Si le jeu prend en charge une option d’installation personnalisée ou avancée, vérifiez que cette option est accessible pendant le processus d’installation.</li>
<li>Vérifiez que l’option d’installation par défaut contourne toutes les sélections d’entrée d’utilisateur pour le processus d’installation (sélection du dossier d’installation, sélection des composants, etc.).</li>
<li>Vérifiez que le processus d’installation du jeu ne demande pas la configuration des composants du système d’exploitation (installation de DirectX, runtimes Visual C, etc.).</li>
<li>Vérifiez que le processus d’installation du jeu ne demande pas d’interaction avec le pare-feu.</li>
<li>Vérifiez que le jeu s’exécute automatiquement ou qu’un menu de lancement est présent à la fin du processus d’installation.</li>
<li>Vérifiez que le processus de désinstallation du jeu supprime tous les fichiers installés et non redistribués des composants du système d’exploitation et efface tous les paramètres. Il n’est pas nécessaire de nettoyer tous les paramètres et données par utilisateur (par exemple, les parties enregistrées).</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="32-support-user-account-control-for-installation"></a>3,2 prendre en charge le contrôle de compte d’utilisateur pour l’installation



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>Le programme d’installation du jeu ne doit pas supposer qu’il s’exécute dans le même contexte que l’utilisateur. Les jeux doivent donc exécuter des tâches par utilisateur lors de la première exécution séparément de l’installation.</td>
</tr>
<tr class="even">

<td><ol>
<li>Vérifiez que vous pouvez installer le jeu en tant qu’utilisateur Jane. (Cela nécessite des droits élevés au cours du processus d’installation/d’installation.)</li>
<li>Vérifiez que le processus d’installation du jeu invite l’utilisateur Jane à élever ses droits d’administrateur. (L’invite à élever s’affiche lorsque l’utilisateur tente d’installer.)</li>
<li>Choisissez d’exécuter automatiquement le jeu à la fin de l’installation, s’il ne le fait pas déjà, ou lancez-le à partir du menu qui s’affiche.</li>
<li>Une fois en jeu, créez un nouveau profil, jouez et enregistrez un jeu.</li>
<li>Quittez le jeu.</li>
<li>Redémarrez le jeu et vérifiez que les profils utilisateur et les jeux enregistrés sont accessibles par le compte utilisateur Jane.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="33-install-to-correct-folders"></a>3,3 installer pour corriger les dossiers



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Les jeux doivent être installés dans le dossier Program Files par défaut. Les données utilisateur doivent être écrites lors de la première exécution et non lors de l’installation.</td>
</tr>
<tr class="even">

<td><ol>
<li>Installez le jeu en utilisant le type d’installation par défaut.</li>
<li>Vérifiez que le jeu a été installé dans Program Files.</li>
</ol>
<blockquote>
[!Note]<br />
Si ce test échoue, vérifiez que le jeu est destiné à être installé pour tous les utilisateurs. Si c’est le cas, il s’agit d’un échec.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="34-install-windows-resources-properly"></a>3,4 installer correctement les ressources Windows



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>les Applications ne doivent pas tenter d’installer des fichiers ou des clés de registre protégés par Protection des ressources Windows (WRP).</td>
</tr>
<tr class="even">

<td><ul>
<li>vérifiez qu’aucune boîte de dialogue Protection des ressources Windows WRP ne s’affiche pendant le processus d’installation.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="35-avoid-reboots-during-installation"></a>3,5 éviter les redémarrages au cours de l’installation



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>le programme d’installation de jeu ne doit pas supposer que l’installation de Windows composants à partir de packages de redistribution nécessite un redémarrage, sauf si le redémarrage est indiqué par un résultat de retour ou par la documentation de Microsoft.</td>
</tr>
<tr class="even">

<td><ol>
<li>Installez le jeu.</li>
<li>Vérifiez que le jeu ne nécessite pas le redémarrage du système après l’installation.</li>
</ol>
<blockquote>
[!Note]<br />
Si un redistribution de la mise à jour Microsoft System requiert un redémarrage, procédez comme suit : terminer l’installation du jeu, désinstaller le jeu et réinstaller le jeu une deuxième fois. Le processus d’installation du jeu ne doit pas nécessiter un redémarrage lors de cette deuxième installation.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="36-use-file-versioning-correctly"></a>3,6 utiliser le contrôle de version de fichier correctement



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Le programme d’installation du jeu doit vérifier correctement si les dernières versions de fichiers sont installées. L’installation d’un jeu ne doit jamais régresser les fichiers que vous ne générez pas ou qui sont partagés par des applications que vous ne générez pas.</td>
</tr>
<tr class="even">

<td><ol>
<li>Avant d’installer le jeu, créez une capture instantanée de préinstallation de system32.<br/>
<ol>
<li>Créez un répertoire appelé G4Wtest.</li>
<li>Afficher une fenêtre de commande (Start-> Run-> cmd).</li>
<li>Accédez à c:\Windows\System32.</li>
<li>Tapez dir/o :-g/o :-d >> c:\G4Wtest\pregame.txt.</li>
</ol></li>
<li>Créez un instantané postérieur à l’installation de system32. <br/>
<ol>
<li>Afficher une fenêtre de commande (Start-> Run-> cmd).</li>
<li>Accédez à c:\Windows\System32.</li>
<li>Tapez dir/o :-g/o :-d >> c:\G4Wtest\postgame.txt.</li>
<li>Vérifiez que le jeu n’a pas pour effet de régresser les versions de fichiers que le jeu n’a pas produit (... des fichiers figurant dans les deux documents en comparant pregame.txt à postgame.txt).</li>
</ol></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="37-support-autorun-conditional-requirement"></a>3,7 prise en charge de l’exigence conditionnelle d’exécution automatique \[\]



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Pour les jeux distribués sur CD, DVD ou tout autre support amovible qui prennent en charge l’exécution automatique, lorsque le disque est inséré pour la première fois, l’application doit automatiquement s’exécuter ou inviter l’utilisateur à installer le jeu. <br/>
<blockquote>
[!Note]<br />
les programmes d’exécution automatique qui ont été écrits pour une utilisation sur des versions de Windows antérieures à Windows Vista ne doivent pas utiliser le runtime .net, car cette technologie n’est pas incluse dans Windows XP ni dans les versions antérieures de Windows.
</blockquote>
<br/> pour plus d’informations, reportez-vous à <a href="/windows/win32/DxTechArts/games-for-windows-technical-requirements-1-1-0006">jeux pour Windows exigences techniques</a> 3,7, Support Autorun. <br/></td>
</tr>
<tr class="even">

<td><ol>
<li>Insérez le disque ou le média du jeu.</li>
<li>Vérifiez que la boîte de dialogue installation/exécution s’affiche automatiquement.</li>
<li>Windows Vista ou Windows 7 : vérifiez que le programme d’exécution automatique de jeu lui-même n’invite pas l’utilisateur Jane à élever ses droits d’administrateur.</li>
<li>Vérifiez que l’exécutable d’exécution automatique n’a pas besoin de composants de redistribution out-of-Box, tels que les bibliothèques .NET 3,5, C Run-Time, etc.</li>
<li>Vérifiez que la réinsertion du disque dans le lecteur après l’installation n’entraîne pas le redémarrage automatique de l’installation.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="4-reliability"></a>4. fiabilité

### <a name="41-eliminate-unnecessary-reboots"></a>4,1 éliminer les redémarrages inutiles



| Système d''exploitation                                              | Condition requise                                                                                                                                                                   |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows 7<br/> Windows Vista<br/> | Tous les programmes d’installation de l’application doivent tirer parti des API du gestionnaire de redémarrage pour éviter les redémarrages du système (voir la [condition 3,5](#35-avoid-reboots-during-installation)). |



 

### <a name="42-eliminate-application-verifier-failures"></a>4,2 éliminer les échecs de Application Verifier



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Le jeu ne doit générer aucun échec s’exécutant sous Microsoft Application Verifier (AppVerifier), version 4,0 ou ultérieure, dans les tests suivants : <br/>
<ul>
<li>Concepts de base : handles, tas, verrous, mémoire, TLS</li>
<li>Divers : DangerousAPIs, DirtyStacks</li>
</ul></td>
</tr>
<tr class="even">

<td>Utiliser l’outil : AppVerifier 4,0 (ou version ultérieure)<br/>
<ol>
<li>Installer AppVerifier.</li>
<li>Lancez AppVerifier et sélectionnez fichier-> ajouter une application.</li>
<li>Recherchez l’exécutable du jeu, sélectionnez-le, puis cliquez sur le &quot; &quot; bouton Ouvrir.</li>
<li>Dans la &quot; &quot; section applications, sélectionnez l’exécutable du jeu.</li>
<li>Dans la &quot; &quot; section tests, sélectionnez les tests répertoriés ci-dessus sous les catégories &quot; concepts &quot; de base et &quot; divers &quot; (décochez ThreadPool et TimeRollOver) et vérifiez que tous les autres tests ne sont pas sélectionnés.</li>
<li>Lancez le jeu.</li>
<li>Vérifiez que le jeu ne génère pas d’erreurs lorsqu’il est exécuté sous Application Verifier.</li>
</ol>
<blockquote>
[!Note]<br />
Certains tests requièrent l’exécution complète d’un débogueur. Cela peut nécessiter une version non protégée de l’exécutable du jeu, car la technologie anti-triche/anti-piratage peut interférer avec AppVerifer.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="43-support-windows-error-reporting"></a>Rapport d’erreurs Windows de Support 4,3



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>les jeux doivent gérer uniquement les exceptions connues et attendues, et la Rapport d’erreurs Windows ne doit pas être désactivée. si une erreur (telle qu’une Violation d’accès) est injectée dans un jeu, elle doit autoriser Rapport d’erreurs Windows à signaler l’incident.</td>
</tr>
<tr class="even">

<td>Utiliser l’outil : détourneur de thread <br/>
<ul>
<li>si l’application se bloque pendant le test, vérifiez que le jeu affiche Rapport d’erreurs Windows correctement et collecte des données de panne.</li>
</ul></td>
</tr>
</tbody>
</table>



 



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Tous les fichiers exécutables (par exemple, les fichiers .exe ou .dll) doivent contenir un nom de produit, un nom de société et une version de fichier précis.</td>
</tr>
<tr class="even">

<td><dl> <dt><span id="Manual_test_"></span><span id="manual_test_"></span><span id="MANUAL_TEST_"></span>Test manuel :</dt> <dd>
<ol>
<li>Cliquez avec le bouton droit sur le ou les fichiers exécutables du jeu sur le support d’installation de et sur ceux qui sont installés sur le disque dur de l’ordinateur.</li>
<li>Sélectionnez Propriétés.</li>
<li>Windows XP : cliquez sur l’onglet <strong>version</strong> . Vérifiez que les champs nom du produit, nom de la société et version du fichier sont correctement remplis.</li>
<li>Windows Vista ou Windows 7 : cliquez sur l’onglet <strong>détails</strong> . Vérifiez que les champs nom du produit et version du fichier sont correctement remplis. le nom de la société n’est pas visible dans la page de propriétés Windows Vista ou Windows 7.</li>
</ol>
</dd> <dt><span id="Automated_test_"></span><span id="automated_test_"></span><span id="AUTOMATED_TEST_"></span>Test automatisé :</dt> <dd>
<ul>
<li>utilisez l’outil de Test jeux Microsoft pour Windows ; consultez la <a href="#64-microsoft-games-for-windows-test-tool">section 6,4</a>.</li>
</ul>
</dd> </dl></td>
</tr>
</tbody>
</table>



 



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>La sortie normale du jeu ne doit pas aboutir à une erreur d’exception inconnue.</td>
</tr>
<tr class="even">

<td><ul>
<li>Après avoir joué le jeu pour une session de jeu normale, vérifiez que le jeu ne génère pas d’erreurs à la sortie.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="5-sample-test-script"></a>5. exemple de script de test

Il s’agit d’un exemple de test typique en utilisant les exigences de test ci-dessus comme guide.

### <a name="51-tools"></a>5,1 outils

-   édition 32 bits de Windows Vista SP1 et/ou Windows 7 sur un processeur AMD
-   édition 32 bits de Windows Vista SP1 et/ou Windows 7 sur un processeur Intel
-   édition 64 bits de Windows Vista SP1 et/ou Windows 7 sur un processeur AMD
-   édition 64 bits de Windows Vista SP1 et/ou Windows 7 sur un processeur Intel
-   édition 32 bits Windows XP SP2 sur un processeur AMD
-   édition 32 bits Windows XP SP2 sur un processeur Intel
-   Moniteur à écran étendu qui prend en charge 1680 1050
-   manette Xbox 360 pour Windows

### <a name="52-pre-install"></a>5,2 pré-installation

1.  Windows Vista et Windows 7 : créer deux utilisateurs Standard : Jane et Toby
2.  Windows Vista et Windows 7 : vérifier que le contrôle de compte d’utilisateur est activé
3.  Créer un instantané de préinstallation de system32

    1.  Créer un répertoire appelé G4Wtest
    2.  Afficher une fenêtre de commande (Start-> Run-> cmd)
    3.  Accédez à c : \\ Windows \\ system32
    4.  Tapez dir/o :-g/o :-d >> c : \\ G4Wtest \\pregame.txt

4.  Windows Vista et Windows 7 : définissez sur 150% ppp \[ 1,8\]
5.  Continuer l' [installation](#3-installation)

### <a name="53-install"></a>installation de 5,3

1.  Ouvrir une session en tant qu’utilisateur Jane
2.  Insérez le disque du jeu dans le lecteur de CD/DVD, vérifiez que la boîte de dialogue installation/exécution s’affiche automatiquement \[ 3,7\]
3.  Vérifiez que le processus d’installation du jeu invite l’utilisateur Jane à élever les informations d’identification de l’administrateur \[ 3,2\]
4.  Vérifiez que le programme d’exécution automatique de jeu lui-même ne demande pas à l’utilisateur Jane d’effectuer une élévation via les informations d’identification d’administrateur \[ 3,7\]
5.  Vérifiez que le jeu n’affiche pas plus d’un contrat de licence End-User (CLUF) \[ 3,1\]
6.  Vérifiez que le jeu affiche les options d’installation par défaut/simples et personnalisées/avancées \[ 3,1\]
7.  Vérifiez que l’option d’installation par défaut/Easy contourne toutes les sélections d’entrée utilisateur pour le processus d’installation (sélection du dossier d’installation, sélection des composants, etc.) \[ . 3,1\]
8.  Vérifiez que le processus d’installation du jeu ne demande pas la configuration des composants du système d’exploitation (installation de DirectX, bibliothèques C Run-Time, etc.) \[ . 3,1\]
9.  Vérifier que le processus d’installation du jeu ne demande pas d’interaction avec le pare-feu \[ 3,1\]
10. Vérifiez que le processus d’installation du jeu ne rencontre pas d’erreur concernant la version \[ 2,5 \] \[ 4,2 du système d’exploitation\]
11. Vérifiez que le processus d’installation du jeu n’affiche pas de boîte (s) de dialogue de pilote non signé \[ 2,4\]
12. vérifiez qu’aucune boîte de dialogue de Protection des ressources Windows (WRP) ne s’affiche pendant le processus d’installation \[ 3,4\]
13. Vérifiez que la réinsertion du disque dans le lecteur après l’installation n’entraîne pas le redémarrage automatique de l’installation
14. Vérifiez que le jeu ne nécessite pas le redémarrage du système après l’installation \[ 3,5\]
15. Vérifiez que vous pouvez installer le jeu en tant qu’utilisateur Jane \[ 3,2\]
16. Vérifiez que le jeu s’exécute automatiquement ou qu’un menu de lancement est présent à la fin du processus d’installation \[ 3,1\]
17. Si le jeu s’exécute automatiquement après l’installation, passez au [Runtime](#55-runtime)
18. Si le jeu a quitté un menu de lancement ou n’a pas pu désinstaller, voir la section [après l’installation](#54-post-install)

### <a name="54-post-install"></a>5,4 après l’installation

1.  Vérifier que le jeu ne place pas de raccourcis de lancement sur le Bureau de l’utilisateur \[ 1,1\]
2.  Vérifiez que le jeu ne place pas de raccourcis de lancement dans le menu démarrer \[ 1,1\]
3.  vérifier que l’icône du jeu s’affiche dans Windows l’explorateur de jeux \[ 1,1\]
4.  Vérifiez que les métadonnées (éditeur, développeur, genre, date de publication, version) s’affichent en bas et qu’elles sont correctes. \[ 1,1\]
5.  vérifiez que l’icône de jeu affiche les informations de l’Index de Windows WEI dans Windows Games Explorer \[ 1,1\]
6.  vérifier que les liens hypertexte de jeu pour les métadonnées fonctionnent correctement dans Windows Games Explorer \[ 1,1\]
7.  vérifier que le jeu affiche une évaluation précise du contrôle parental dans Windows Games Explorer \[ 1,1\]
8.  Créer un instantané postérieur à l’installation de system32

    1.  Afficher une fenêtre de commande (Start-> Run-> cmd)
    2.  Accédez à c : \\ Windows \\ system32
    3.  Tapez dir/o :-g/o :-d >> c : \\ G4Wtest \\postgame.txt
    4.  Vérifiez que le jeu ne régresse pas les versions de fichiers listées dans les deux documents en comparant pregame.txt à postgame.txt \[ 3,6\]

9.  Passer au [Runtime](#55-runtime)

### <a name="55-runtime"></a>Runtime 5,5

1.  RUNTIME 1 : si le menu de lancement est présent, lancez le jeu à partir de là. Si le jeu a été exécuté automatiquement ou a été lancé à partir du menu du lanceur de jeux après l’installation, procédez comme suit : Si ce n’est pas le cas, passez au RUNTIME 2 :

    1.  Créer un profil (si le jeu le permet)
    2.  Démarrer un nouveau jeu
    3.  Enregistrer le jeu
    4.  Quitter le jeu
    5.  Lancer le jeu à partir de l’Explorateur de jeux
    6.  Vérifier que le jeu est lancé à partir de l’icône de l’Explorateur de jeux \[ 1,2\]
    7.  Vérifiez que le jeu ne demande pas les informations d’identification de l’administrateur au lancement de \[ 1,2\]
    8.  Vérifier que les profils utilisateur et l’enregistrement des jeux sont accessibles par l’utilisateur Jane compte \[ 3,2\]
    9.  Passer au RUNTIME 3

2.  RUNTIME 2 : si le jeu n’a pas été exécuté automatiquement ou si vous affichez un lancement à partir du menu du lanceur de jeu, il s’agit d’une défaillance de \[ 3,1 \] ; Toutefois, le test peut se poursuivre normalement :

    1.  Lancer le jeu à partir de l’Explorateur de jeux
    2.  Vérifier que le jeu est lancé à partir de l’icône de l’Explorateur de jeux \[ 1,2\]
    3.  Vérifiez que le jeu ne demande pas les informations d’identification de l’administrateur au lancement de \[ 1,2\]
    4.  Passer au RUNTIME 3

3.  RUNTIME 3 : si le jeu prend en charge un boîtier de jeu, vérifiez que le jeu reconnaît manette Xbox 360 pour Windows en tant qu’appareil d’entrée \[ 1,4\]

    1.  Si nécessaire, activez le contrôleur via le menu options.
    2.  Vérifier que le jeu fait référence aux boutons et aux déclencheurs de contrôleur à l’aide des noms Xbox 360
    3.  vérifiez que le jeu et le système de menus sont contrôlable avec la manette Xbox 360 pour Windows
    4.  vérifier que le manette Xbox 360 pour Windows se comporte conformément aux normes acceptées

4.  Définissez la vidéo sur \[ 1,5 \] :

    1.  Vérifier que le jeu s’exécute à une résolution de 4:3 de proportions (800 600 ou 1024 768)
    2.  Vérifier que le jeu s’exécute à une résolution de proportions 16:9 (1280 720)
    3.  Vérifier que le jeu s’exécute à une résolution de proportions 16:10 (1680 1050, 800 480 ou 1152 720)
    4.  Vérifier que le jeu demande à l’utilisateur quand une modification est apportée à la résolution
    5.  Vérifiez que l’affichage revient au paramètre précédent si vous n’acceptez pas dans les 15 secondes.
    6.  Vérifier que le jeu n’étire pas l’image et, à son tour, présente une zone de vue plus vaste
    7.  Vérifier que le jeu n’ajoute pas de barres noires à gauche et à droite de la zone de jeu

5.  S’il est disponible dans les paramètres vidéo, vérifiez que les options de rendu du jeu sont par défaut Direct3D \[ 1,7 \] ; sinon, passez à [tests automatisés](#58-automated-tests)
6.  Si vous y êtes invité ou si l’option est disponible, créez un profil utilisateur. Vérifier que le jeu ne rencontre pas d’erreurs lors de l’utilisation de noms de fichiers longs \[ 2,7\]
7.  Démarrez un nouveau jeu, créez un jeu et vérifiez que le jeu ne rencontre pas d’erreurs lors de la gestion des caractères de système de fichiers non pris en charge \[ 2,7\]
8.  vérifiez que le jeu est correctement ALT + tabulations sur le Windows desktop \[ 2,6\]

    1.  Permuter les utilisateurs avec le jeu en cours d’exécution en cliquant sur Démarrer-> changer d’utilisateur
    2.  Ouvrir une session en tant que Toby
    3.  Vérifiez que le jeu démarre en tant qu’utilisateur Toby, tout en étant toujours en cours d’exécution en tant qu’utilisateur Jane \[ 2,6\]
    4.  Vérifier que le jeu ne rencontre pas d’erreurs pour l’utilisateur Toby ou l’utilisateur Jane pendant le processus de changement d’utilisateur \[ 2,6\]
    5.  Vérifiez que vous ne pouvez pas entendre l’audio de la session de jeu d’origine \[ 2,6\]
    6.  Quitter le jeu
    7.  Fermer la session Toby
    8.  Revenir à l’utilisateur d’origine sur lequel le jeu est en cours d’exécution
    9.  ALT + TAB de nouveau dans le jeu

9.  Quitter le jeu
10. Passer au [Runtime](#56-post-runtime)

### <a name="56-post-runtime"></a>5,6 après le Runtime

1.  Vérifier que le jeu ne génère pas d’erreurs à la sortie \[ 4,3\]
2.  Vérifier que le jeu est installé dans Program Files \[ 3,3\]
3.  Passer aux [contrôles de contrôle parental](/windows)

### <a name="57-parental-controls"></a>5,7 contrôle parental

1.  Ouvrir le contrôle parental dans le panneau de configuration
2.  Vérifiez que le jeu affiche une évaluation exacte du contrôle parental sous le titre du jeu dans le panneau de configuration du contrôle parental \[ 1,2\]
3.  Consultez le cas \[ de Test 1,2 \] pour les tests suivants :

    1.  Après avoir défini le contrôle parental sur « on », vérifiez que le jeu s’exécute avec ces paramètres en tant qu’utilisateur Jane \[ 1,2\]
    2.  Déconnectez-vous et ouvrez une session en tant que Toby
    3.  Vérifiez que le jeu s’exécute avec ces paramètres en tant qu’utilisateur Toby \[ 1,2\]
    4.  Déconnectez-vous et ouvrez une session en tant que Jane
    5.  Dans la section contrôle parental, empêchez l’utilisateur Toby de voir les jeux un niveau ESRB supérieur et supérieur du jeu que vous venez d’installer.

        Exemple : si le jeu est évalué E, définissez-le de sorte que Toby ne puisse jouer que des jeux classés en C

    6.  Vérifiez que le jeu s’exécute avec ces paramètres en tant qu’utilisateur Jane \[ 1,2\]
    7.  Fermer la session et ouvrir une session en tant qu’utilisateur Toby
    8.  Vérifier que le jeu n’est pas lancé sur l’utilisateur Toby lorsque ESRB est bloqué par l’utilisateur Jane \[ 1,2\]
    9.  Déconnectez-vous en tant qu’utilisateur Toby et reconnectez-vous en tant qu’utilisateur Jane
    10. En cas de modification précédente, restaurez les paramètres ESRB
    11. S’il n’existe aucun paramètre ESRB, sélectionnez « bloquer ou autoriser des jeux spécifiques », puis sélectionnez le jeu par son nom.
    12. Déconnectez-vous en tant que Jane et en tant que Toby
    13. Vérifier que le jeu n’est pas lancé sur l’utilisateur Toby lorsque l’utilisateur ou le nom est bloqué par l’utilisateur Jane \[ 1,2\]
    14. Déconnectez-vous en tant que Toby et revenez sous le titre Jane
    15. Pour Jane, ouvrez contrôles utilisateur-> restrictions d’application
    16. Cliquez sur « Toby ne peut utiliser que les programmes que je peux autoriser », puis cliquez sur OK (c’est-à-dire n’autoriser aucun exe)
    17. Cliquez sur la case décocher tout, puis sur OK.
    18. Accéder à l’utilisateur contrôle les \| contrôles des jeux et autoriser le jeu spécifique à utiliser l’évaluation de la ESRB
    19. Déconnectez-vous en tant que Jane et connectez-vous en tant que Toby et essayez de jouer au jeu
    20. Vérifiez que le jeu n’est pas bloqué et que Toby peut le lire quand « n’autoriser aucun exe » est défini \[ 1,2\]
    21. Déconnectez-vous en tant qu’utilisateur Toby et reconnectez-vous en tant qu’utilisateur Jane
    22. Accédez à contrôle parental dans le panneau de configuration et supprimez les restrictions
    23. Vérifier que les deux utilisateurs peuvent maintenant jouer au jeu

4.  Passer aux [tests automatisés](#58-automated-tests)

### <a name="58-automated-tests"></a>5,8 tests automatisés

1.  Vérifiez que le jeu ne génère pas d’erreurs lorsqu’il est exécuté sous Application Verifier-consultez documentation de l’outil de test de personnalisation \[ 4,2\]
2.  Vérifiez que les fichiers exécutables du jeu contiennent des manifestes. consultez la documentation de l’outil de test de personnalisation \[ 2,1\]
3.  Vérifiez que le manifeste de fichier exécutable du jeu requestedExecutionLevel est « asInvoker ». consultez la documentation de l’outil de test de personnalisation \[ 2,1\]
4.  Passer à d' [autres tests](#59-other-tests)

### <a name="59-other-tests"></a>5,9 autres tests

1.  Vérifiez que les fichiers exécutables du jeu contiennent une signature numérique \[ 2,3\]
2.  vérifiez que le processus d’installation du jeu s’exécute normalement sur les éditions 64 bits de Windows Vista et/ou Windows 7 \[ 2,3\]
3.  vérifiez que le jeu ne rencontre pas d’erreur en raison d’exécutables 16 bits sur les éditions 64 bits de Windows Vista et/ou Windows 7 \[ 2,3\]
4.  forcer l’application à se bloquer pendant le test et vérifier que le jeu affiche Rapport d’erreurs Windows correctement et collecte les données de panne \[ 4,3\]
5.  Garantir des résumés de fichiers appropriés \[ 4,3\]

    1.  Cliquez sur Démarrer-> un ordinateur
    2.  Accédez au répertoire du jeu
    3.  Dans la fenêtre de recherche, tapez \*.dll
    4.  Pour chaque fichier : cliquez avec le bouton droit sur le fichier, puis cliquez sur Propriétés.

        -   dans Windows XP : cliquez sur l’onglet Version. Vérifiez que les champs nom du produit, nom de la société et version du fichier sont correctement remplis. \[4.3\]
        -   dans Windows Vista et Windows 7 : cliquez sur l’onglet détails. Vérifiez que les champs nom du produit et version du fichier sont correctement remplis. le nom de la société n’est pas visible dans la page de propriétés Windows Vista ou Windows 7 \[ 4,3\]

    5.  Répétez cette vérification pour les fichiers .exe

6.  Lancez le jeu.

    1.  Appuyez sur CTRL + ALT + SUPPR
    2.  Cliquez sur la flèche « Options d’arrêt »
    3.  Cliquez sur redémarrer
    4.  Vérifier que le jeu ne bloque pas l’arrêt \[ 3,1\]

7.  Continuer la [désinstallation](#510-uninstall)

### <a name="510-uninstall"></a>désinstallation de 5,10

-   Vérifiez que le processus de désinstallation du jeu supprime tous les fichiers de composants du système d’exploitation non redistribués installés et efface tous les paramètres \[ 3,1\]

    -   vérifiez dans Windows Vista ou Windows 7 que le panneau de configuration est le seul moyen de supprimer le programme \[ 1,1\]

## <a name="test-tool-notes"></a>Notes de l’outil de test

Voici quelques remarques pour chacun des outils de test répertoriés dans les spécifications de test ci-dessus.

### <a name="61-appverifier-40-or-higher"></a>6,1 AppVerifier 4,0 (ou version ultérieure)

**Cas de test : 2,5, 4,2**

> [!Note]  
> Certaines applications ne peuvent pas s’exécuter avec AppVerifier en cours d’exécution, en raison de la protection contre la copie. Cela peut être résolu en exécutant avec une version non protégée de l’exécutable du jeu.

 

1.  installer AppVerifier 4,0 (ou version ultérieure) sur un ordinateur exécutant Windows XP
2.  Lancez AppVerifier et cliquez sur fichier-> ajouter une application
3.  Recherchez l’exécutable du jeu, sélectionnez-le, puis cliquez sur Ouvrir.
4.  Dans la section « applications », sélectionnez l’exécutable du jeu
5.  Dans la section « principes de base », sélectionnez les tests suivants :

    -   Poignées
    -   Tas
    -   Verrous
    -   Mémoire
    -   TLS

6.  Sélectionnez les tests suivants dans la section « divers » :

    -   DangerousAPIs
    -   DirtyStacks

7.  Vérifiez que tous les autres tests ne sont pas sélectionnés
8.  Lancer le jeu
9.  Jouer au jeu
10. Fermer le jeu
11. Dans AppVerifier, sélectionnez Afficher-> les journaux
12. Dans la section « applications », sélectionnez le fichier d' .exe d’application.
13. Dans la section « journaux », sélectionnez le fichier journal et observez le nombre d’erreurs. S’il n’y a pas d’erreurs, terminez les tests AppVerifier. Si des erreurs se produisent, cliquez sur le bouton afficher.
14. Rechercher le document (CTRL + F) comme gravité = "erreur
15. Créer des bogues basés sur la partie NomCouche = de l’échec

### <a name="62-manifest-test---mtexe"></a>6,2 manifeste de test-mt.exe

**Cas de test : 1,8, 2,1**

Cet outil est exécuté à partir d’une invite de commandes à l’emplacement où se trouve MT.exe.

Exemple :

``` syntax
mt.exe -inputresource:"c:\yourdir\YourGame.exe";#1 -out:yourgame.manifest
```

1.  Cliquez sur Démarrer-> exécuter-> tapez cmd et cliquez sur le bouton OK
2.  Exécutez l’outil mt.exe pour générer un fichier. manifest pour chaque fichier .exe qui est installé avec le jeu.
3.  Ouvrir le fichier. manifest généré
4.  Vérifiez que chaque fichier .exe contient les éléments suivants (demandés :

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
> Le niveau d’exécution demandé doit être présent pour chaque fichier, et dpiAware doit être présent pour au moins le fichier exécutable du jeu.

 

### <a name="63-thread-hijacker---threadhijackerexe"></a>détourneur de thread 6,3-threadhijacker.exe

Cet outil est exécuté à partir d’une invite de commandes à l’emplacement où se trouve threadhijacker.exe.

Exemple :

``` syntax
threadhijacker.exe /process:str
```

Où str est le nom \_ de \_program.exe

1.  Affichez le gestionnaire des tâches, cliquez sur l’onglet processus, puis recherchez le nom de l’exécutable du jeu.
2.  Ouvrir une invite de commandes en mode administrateur
3.  Accédez au répertoire où threadhijacker.exe est
4.  Type : **threadhijacker.exe/process :** Str, où str est le nom de l’exécutable que vous souhaitez atteindre.

### <a name="64-microsoft-games-for-windows-test-tool"></a>6,4 jeux Microsoft pour l’outil de Test Windows

Cet outil se trouve dans le kit de développement logiciel (SDK) DirectX. une fois le kit de développement logiciel (SDK) installé sur un ordinateur, le programme d’installation de l’outil de test Games for Windows peut être placé sur l’ordinateur de test et installé.

localisez le programme d’installation de Microsoft Games for Windows Test Tool sur l’ordinateur de développement sur lequel le kit SDK DirectX est installé. Par défaut, il est placé à l’emplacement suivant :

``` syntax
%SystemDrive%\Program Files (x86)\Microsoft DirectX SDK (Date)\Utilities\bin\x86\Microsoft Games for Windows Test Tools\
```

1.  Copiez le programme d’installation (MicrosoftGFWTestTool.msi/setup.exe) sur l’ordinateur de test.
2.  Exécutez le programme d’installation.
3.  lancez l’outil de Test jeux Microsoft pour Windows.
4.  dans le champ de **liste Project** , remplacez **create new Project** par le nom de votre titre, puis cliquez sur **create new**.

    Attendez la fin de la ligne de base.

5.  Renseignez toutes les informations que vous pouvez avoir dans la section informations sur le **jeu** , puis cliquez sur **mettre à jour les informations de jeu**.
6.  Cliquez sur l’onglet **cas de test** .
7.  En commençant par le haut, suivez les cas de test, en cliquant sur **réussite** ou **échec** , le cas échéant.

    Pour plus d’informations sur l’inclusion d’un bogue dans le rapport, consultez « écriture d’un bogue », plus loin dans cette section.

8.  Revenez à l’onglet **projets** après avoir consulté le rapport (en vérifiant les onglets **rapport** et **modification des bogues** ).
9.  Cliquez sur **compiler le rapport**.

    Une fenêtre s’ouvre lorsque la compilation du rapport est terminée. Vous trouverez ici un .ZIP noms de fichiers *nom_projet* \_report.zip. Ce fichier contient tous les journaux et résultats collectés pendant la réussite du test.

### <a name="writing-a-bug"></a>Écriture d’un bogue

Il existe deux façons d’écrire un rapport de bogue : vous pouvez parcourir les cas de test et cliquer sur **échec** lorsque le titre échoue à un cas de test, ou vous pouvez cliquer sur l’onglet **modifier un bogue** et ajouter manuellement un rapport de bogue.

### <a name="clicking-fail-on-a-test-case"></a>Cliquer sur échec dans un cas de test

1.  Lorsque vous cliquez sur **échec** dans un cas de test, la liste déroulante **type de problème** est automatiquement définie sur le type de cas de test.
2.  Ajoutez une courte description au champ **titre** qui décrit brièvement le problème.
3.  Ajoutez une description détaillée du problème au champ **comportement observé** .
4.  Le cas échéant, ajoutez ce qui était attendu (par opposition à une description du problème) au champ **comportement attendu** .
5.  Ajoutez une description détaillée de la façon de reproduire le problème dans le champ **reproduction-étapes** .
6.  Lorsque vous avez terminé, cliquez sur le bouton **Enregistrer** .

### <a name="manually-adding-a-bug"></a>Ajout manuel d’un bogue

Ce processus revient à cliquer sur **échec**, à l’exception de la liste déroulante de remplissage automatique. Dans ce cas, sélectionnez le type d’échec TCR approprié ou sélectionnez un **\* \* problème \* \* non-TR** pour les bogues qui se trouvent en dehors de la plage TR mais qui doivent toujours être signalés.

## <a name="resources"></a>Ressources

<dl> <dt>

<span id="Games_for_Windows__Technical_Requirements"></span><span id="games_for_windows__technical_requirements"></span><span id="GAMES_FOR_WINDOWS__TECHNICAL_REQUIREMENTS"></span>jeux pour Windows : exigences techniques
</dt> <dd>

[jeux pour Windows exigences techniques : meilleures pratiques pour les jeux sur Windows XP, Windows Vista et Windows 7](./games-for-windows-technical-requirements-1-1-0006.md)

</dd> <dt>

<span id="Windows_SDK"></span><span id="windows_sdk"></span><span id="WINDOWS_SDK"></span>Windows SDK
</dt> <dd>

[Windows Kits](https://msdn.microsoft.com/bb980924.aspx)

</dd> <dt>

<span id="User_Account_Control_Guidelines"></span><span id="user_account_control_guidelines"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES"></span>Instructions relatives au contrôle de compte d’utilisateur
</dt> <dd>

[Windows Conditions requises pour le développement d’applications Vista pour la compatibilité du contrôle de compte d’utilisateur](/previous-versions/dotnet/articles/bb530410(v=msdn.10))

</dd> <dt>

<span id="Windows_Installer_Information"></span><span id="windows_installer_information"></span><span id="WINDOWS_INSTALLER_INFORMATION"></span>Windows Informations sur le programme d’installation
</dt> <dd>

[Windows Installer](../msi/windows-installer-portal.md)

</dd> <dt>

<span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>Portail des développeurs WinQual 
</dt> <dd>

[Windows Services en ligne de qualité (winqual)](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)

</dd> <dt>

<span id="DirectX_Developer_Portal"></span><span id="directx_developer_portal"></span><span id="DIRECTX_DEVELOPER_PORTAL"></span>Portail des développeurs DirectX
</dt> <dd>

[Centre de développement DirectX](/previous-versions/windows/apps/hh452744(v=win.10))

</dd> <dt>

<span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Blog sur les jeux pour Windows et DirectX SDK
</dt> <dd>

[Jeux pour Windows et kit de développement logiciel (SDK) DirectX](https://walbourn.github.io/)

</dd> <dt>

<span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Autres articles DirectX
</dt> <dd>

[Articles techniques sur DirectX](./dx9-technical-articles.md)

</dd> </dl>

 

