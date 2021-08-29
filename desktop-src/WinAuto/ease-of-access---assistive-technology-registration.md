---
title: Inscription aux technologies d’assistance d’ergonomie
description: Cet article explique comment inscrire une application d’accessibilité à l’aide de la facilité d’accès du centre d’accès. Il explique également comment adapter votre application d’accessibilité de manière à ce qu’elle fonctionne correctement avec le Bureau sécurisé.
ms.assetid: 6F1F2AAE-B2E4-4F26-8BDF-A3DE8F5C5460
ms.topic: article
ms.date: 04/02/2019
ms.openlocfilehash: 9a87fadac85906dfd07fd4c568185125039207d9
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885201"
---
# <a name="ease-of-access---assistive-technology-registration"></a>Inscription aux technologies d’assistance d’ergonomie

Cet article explique comment inscrire une application d’accessibilité à l’aide de la facilité d’accès du centre d’accès. Il explique également comment adapter votre application d’accessibilité de manière à ce qu’elle fonctionne correctement avec le Bureau sécurisé.

la facilité d’accès est une application de panneau de configuration pour Microsoft Windows qui rassemble des fonctionnalités d’accessibilité et de facilité d’utilisation. Grâce à la facilité d’accès, les utilisateurs peuvent configurer leurs ordinateurs en fonction de leurs besoins physiques et cognitifs.

L’une des fonctions de la facilité d’accès du centre d’accès est d’aider les utilisateurs à lancer des applications d’accessibilité, notamment le narrateur, le clavier visuel et la loupe. Les applications tierces inscrites apparaissent également dans la facilité d’accès du centre d’accès et peuvent être lancées directement à partir de là.

Les applications d’accessibilité doivent fonctionner correctement avec le Bureau sécurisé. Le Bureau sécurisé est l’interface utilisateur qui s’affiche lorsque l’ordinateur est verrouillé (au moment de l’ouverture de session ou lorsque l’utilisateur a verrouillé le bureau), et lorsque l’utilisateur est invité à autoriser une action potentiellement dangereuse. pour des raisons de sécurité, Windows place des limites sur les logiciels tiers s’exécutant sur le bureau sécurisé. Si vous souhaitez que votre application d’accessibilité s’exécute sur le Bureau sécurisé, vous devez inscrire l’application à l’aide de la facilité d’accès du centre d’accès.

## <a name="registering-with-the-ease-of-access-center"></a>Inscription avec la facilité d’accès du centre d’accès

Les applications d’accessibilité s’inscrivent dans la facilité d’accès du centre d’accès en créant une ou plusieurs clés de registre lors de l’installation de l’application. Le tableau suivant répertorie les informations contenues dans les clés de registre.



| Name                        | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | Obligatoire/facultatif | Langage      |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|---------------|
| Nom de l’application            | Nom de l’application, qui se trouve dans un fichier de ressources. Cette valeur de registre contient une chaîne dans un format spécifié. Il peut s’agir d’une version localisée du nom de l’application, si l’application est localisée dans une langue autre que l’anglais. Le nom s’affiche dans la facilité d’accès du centre d’accès.<br/>                                                                                                                                                                                                                                                                                       | Obligatoire          | Localisée     |
| ATExe                       | Nom de l’image ou du fichier exécutable de l’application. Windows utilise cette valeur pour déterminer si l’application d’accessibilité est en cours d’exécution.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            | Obligatoire          | Non localisé |
| CopySettingsToLockedDesktop | Valeur **DWORD** qui indique s’il faut copier les paramètres de l’application d’accessibilité sur le bureau verrouillé.<br/> si cette valeur est 1, l’application peut écrire des paramètres dans le registre de l’utilisateur, et Windows copie les paramètres dans le même emplacement dans le registre de l’utilisateur pour le bureau verrouillé. Cela permet à l’application de conserver son état du bureau « normal » sur le bureau verrouillé.<br/>                                                                                                                                                             | Facultatif           | Non localisé |
| Description                 | Brève description de l’application, à partir d’un fichier de ressources. Cette valeur de registre contient une chaîne dans un format spécifié. Il peut s’agir d’une version localisée de la description, si l’application est localisée dans des langues autres que l’anglais. La longueur de cette chaîne doit être inférieure à 512 caractères.<br/> La description s’affiche dans la facilité d’accès du centre d’accès pour fournir à l’utilisateur des informations supplémentaires sur l’application d’accessibilité.<br/> Cette valeur peut également être utilisée pour informer l’utilisateur que l’application n’est pas utilisée sur le Bureau sécurisé.<br/>      | Obligatoire          | Localisée     |
| Profil                     | Bref morceau de code XML qui spécifie les logements fournis par l’application. Il garantit que l’application apparaît sous la catégorie appropriée dans la section facilité d’accès du centre d’accès.<br/>                                                                                                                                                                                                                                                                                                                                                                                                  | Obligatoire          | Non localisé |
| PassiveAutoStartBehavior    | <p>Valeur **DWORD** qui indique si le comportement de démarrage automatique hérité est activé.</p><p>La valeur par défaut est 0, ce qui indique qu’un à nécessite un comportement de démarrage automatique hérité. Dans ce cas, le paramètre « démarrer après la connexion » de ce paramètre est activé dans l’OOBE (out of Box Experience) et le panneau de configuration (voir **panneau de configuration-> facilité d’accès-> facilité d’accès du centre d’accès-> modifier les paramètres de connexion**) et démarre automatiquement le à après l’affichage de l’UAC et l’écran de verrouillage.</p><p>La valeur 1 indique que le à doit utiliser le nouveau comportement de démarrage automatique lorsque le paramètre « démarrer après la connexion » de cet emplacement n’est pas activé dans l’expérience OOBE (out of Box Experience) et le panneau de configuration, et que le est démarré automatiquement une fois par session utilisateur (au moment de la connexion) uniquement si le paramètre « démarrer après la connexion » est activé.</p>                                                                                                                                                                                                                                                                                                                                                                                                  | Facultatif          | Non localisé |
| SecureDesktopAccommodation  | Nom d’une autre application d’accessibilité à exécuter sur le Bureau sécurisé à la place de cette application. l’alternative peut être une application différente, une version différente de la même application, l’une des applications d’accessibilité qui est incluse dans Windows, ou « none » si vous ne souhaitez pas exécuter une application d’accessibilité sur le bureau sécurisé. <br/>                                                                                                                                                                                                               | Facultatif           | Non localisé |
| Profil simple              | Valeur qui décrit comment classer l’application dans un ou deux mots : un lecteur d’écran, une loupe ou un clavier visuel, par exemple.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Obligatoire          | Non localisé |
| Variable startexe                    | Chemin d’accès complet de l’exécutable. Cette valeur est utilisée pour lancer l’application d’accessibilité.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | Obligatoire          | Non localisé |
| StartParams                 | Arguments de ligne de commande Ces valeurs sont utilisées avec variable startexe pour démarrer l’application.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Facultatif           | Non localisé |
| TerminateOnDesktopSwitch    | Valeur **DWORD** qui spécifie la manière dont l’application d’accessibilité répond aux transitions vers ou à partir du Bureau sécurisé.<br/> si cette valeur n’existe pas ou est 1, Windows se termine et redémarre l’application à chaque transition vers ou à partir du bureau sécurisé. Il s'agit du comportement par défaut.<br/> si cette valeur est 0, Windows ne met pas fin à l’application d’accessibilité sur une transition de bureau. l’application continue de s’exécuter sur le poste de travail précédent, et Windows démarre une nouvelle instance sur le nouveau bureau si aucune instance n’est déjà en cours d’exécution.<br/> | Facultatif           | Non localisé |


 

### <a name="localization"></a>Localisation

les valeurs de registre du nom et de la Description de l’Application doivent être localisables pour prendre en charge les interface utilisateur multilingue (MUI).

Ces chaînes sont au format suivant, où les crochets pointent les éléments requis et les crochets signifient un élément facultatif.

*@ <ResDllPath \\ ResDLLFilename>,- &lt; resID &gt; \[ ; &lt; Commentaire&gt;\]*

*<ResDllPath \\ ResDLLFilename>* est le chemin d’accès à la dll de ressource. Le chemin d’accès peut contenir des variables d’environnement.

*&lt; resID &gt;* est l’ID de ressource de la chaîne.

le *\[ Commentaire \]* contient des commentaires facultatifs.

Voici un exemple :


```
@%SystemRoot%\system32\anyAT.dll,-5020
```



pour plus d’informations sur mui, voir [centre de connaissances Windows mui](../intl/about-multilingual-user-interface.md).

### <a name="hci-profile"></a>Profil HCI

Le profil HCI est un moyen de déterminer les logements à fournir en fonction des besoins de l’utilisateur. Les applications d’accessibilité doivent enregistrer des informations sur le type de handicap que l’application aide à prendre en charge.

La valeur de Registre du profil contient du code XML qui décrit le type d’invalidité ciblé par l’application d’accessibilité. Ce code XML a le format suivant :


```XML
<HCIModel>
<Accommodation type="disability"/>
</HCIModel>
```



Les valeurs valides pour l’attribut de **type d’hébergement** sont les suivantes :

-   vision légère
-   vision sérieuse
-   cognitive légère
-   grave cognitive
-   dextérité légère
-   dextérité grave
-   audition légère
-   audition grave
-   discours modéré
-   discours grave

> [!Note]  
> Ces valeurs respectent la casse.

 

Si une application d’accessibilité prend en charge plusieurs logements, la valeur de registre de profil doit inclure un attribut de **type d’hébergement** pour chaque hébergement.

### <a name="ease-of-access-registry-details"></a>Détails du registre d’ergonomie

Pour inscrire votre application d’accessibilité, vous devez créer une clé pour votre application à l’emplacement de Registre suivant et la remplir avec des paires nom-valeur.

**HKLM \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ accessibility \\ ATs\\**

Nommez la clé de registre de votre application en utilisant le format suivant :

*« CompanyName \_ ProductName \_ v \# »*

Par exemple, « Contoso \_ magnifier \_ v 2.0 ».

Pour ajouter des valeurs de Registre, votre programme d’installation doit être exécuté avec des privilèges élevés.

### <a name="secure-desktop-accommodation"></a>Hébergement de postes de travail sécurisé

La clé de Registre **SecureDesktopAccommodation** vous permet de spécifier la manière dont votre application d’accessibilité répond au Bureau sécurisé. Par défaut, le centre d’ergonomie lance votre application sur le Bureau sécurisé s’il était déjà en cours d’exécution sur le bureau normal, ou s’il est configuré pour s’exécuter sur le Bureau d’ouverture de session. À l’aide de la clé **SecureDesktopAccommodation** , vous pouvez :

-   Spécifiez une autre version de votre application pour une utilisation sur le Bureau sécurisé. Par exemple, vous pouvez avoir une autre version qui désactive les fonctionnalités non sécurisées ou qui est optimisée pour utiliser moins de mémoire et démarrer plus rapidement.

    Pour spécifier la version alternative, définissez la clé **SecureDesktopAccommodation** sur le nom de l’autre version. Par exemple, si vous avez inscrit votre application à la \_ clé de lecteur d’écran Contoso \_ v 1.0, vous pouvez inscrire la version alternative sur l' \_ écran contoso ReaderSecure \_ v 1.0. Ensuite, définissez la clé **SecureDesktopAccommodation** du \_ lecteur d’écran Contoso \_ v 1.0 sur « Contoso \_ Screen ReaderSecure \_ v 1.0 ».

-   Spécifiez une application d’accessibilité Microsoft à utiliser sur le Bureau sécurisé à la place de votre application. Pour cette option, définissez **SecureDesktopAccommodation** sur le nom de l’application d’accessibilité Microsoft : « OSK », « magnifierpane » ou « Narrator ».
-   Spécifiez que votre application ne doit pas s’exécuter sur le Bureau sécurisé et aucune autre application. Pour cette option, affectez à **SecureDesktopAccommodation** la valeur « None » (recommandé) ou le nom d’une application inexistante.

si la clé de registre **SecureDesktopAccommodation** pour votre application d’accessibilité spécifie une application d’accessibilité Microsoft à exécuter sur le bureau sécurisé à la place de votre application, Windows en avertit l’utilisateur lors de la transition vers le bureau sécurisé. pour avertir l’utilisateur, Windows affiche la chaîne spécifiée dans la clé de registre Description de votre application. Par exemple, si l’application ScreenReader Deluxe 1,0 utilise le narrateur Microsoft sur le Bureau sécurisé, elle inclut une chaîne de description telle que « Microsoft Narrator sera utilisé dans les bureaux verrouillés, de connexion et autres postes de travail sécurisés à la place de ScreenReader Deluxe 1,0 ».

Si la clé **SecureDesktopAccommodation** de votre application est définie sur « None », utilisez la clé **Description** pour indiquer à l’utilisateur que votre application n’est pas disponible sur le Bureau sécurisé et qu’aucune autre solution n’est fournie.

Windows affiche le texte de Description aux emplacements appropriés dans la facilité d’accès du centre d’accès.

### <a name="running-at-installation-and-on-the-logon-desktop"></a>En cours d’exécution au moment de l’installation et sur le Bureau d’ouverture de session

si vous ajoutez le nom de clé inscrite de votre application d’accessibilité à la chaîne à l’emplacement de registre suivant, Windows lance votre application immédiatement après son installation. en outre, Windows exécute automatiquement votre application chaque fois que le bureau d’ouverture de session est actif.

**\\Configuration de \\ l' \\ \\ accessibilité CurrentVersion Software Microsoft Windows NT \\ \\**

La clé de configuration est une chaîne délimitée par des virgules. pour ajouter votre application, ajoutez une chaîne identique à celle de la clé de registre de votre application dans HKLM \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ accessibility \\ ATs \\ .

### <a name="running-in-a-job"></a>Exécution dans un travail

si la clé de registre **TerminateOnDesktopSwitch** est absente ou si elle est définie sur une valeur différente de zéro, Windows exécute l’application dans le contexte d’un travail, en terminant et en redémarrant l’application avec chaque transition de bureau. L’exécution dans un travail garantit qu’une seule instance de l’application s’exécute à un moment donné et libère l’application de l’analyse de l’état du bureau. Les inconvénients liés à l’exécution d’un travail sont les suivants :

-   L’application entraîne un coût de démarrage avec chaque transition de bureau.
-   L’application peut être démarrée uniquement par le biais de la facilité d’accès du centre d’accès.
-   L’application doit continuellement enregistrer ses paramètres, car elle peut être arrêtée à tout moment par une transition sur le bureau.

si la clé **TerminateOnDesktopSwitch** existe et est définie sur 0, Windows n’exécute pas l’application d’accessibilité dans un travail. Les avantages sont les suivants :

-   Aucun coût de démarrage n’est associé aux transitions sur le bureau.
-   L’application peut être démarrée en dehors de la facilité d’accès du centre d’accès.

Les inconvénients liés à l’absence de fonctionnement dans un travail sont les suivants :

-   Étant donné que l’application n’est pas redémarrée lors des transitions sur le bureau, elle doit détecter le moment où le Bureau actuel est inactif et y répondre de manière appropriée. Par exemple, l’application doit renoncer au contrôle du matériel afin que la version de bureau sécurisée de l’application puisse l’utiliser, et l’application doit passer en mode veille pour éviter d’utiliser les ressources du processeur.
-   si l’application peut être démarrée à l’aide de l’menu Démarrer, Windows Explorer ou la ligne de commande, la facilité d’accès du centre d’accès doit être informée. pour plus d’informations, consultez **Windows Logo key + U**.
-   Étant donné que plusieurs copies de l’application peuvent s’exécuter simultanément sur différents bureaux, l’application doit être écrite pour prendre en charge plusieurs copies en cours d’exécution.

### <a name="windows-logo-key--u"></a>Windows Touche de logo + U

Si votre application d’accessibilité est configurée pour s’exécuter dans un travail, le code de démarrage de votre application doit inclure un appel à la fonction [**IsProcessInJob**](/windows/desktop/api/jobapi/nf-jobapi-isprocessinjob) pour déterminer si l’application démarre dans un travail. Si c’est le cas, l’application doit démarrer l’ergonomie du centre d’accès, puis quitter. L’exemple suivant montre comment appeler **IsProcessInJob**.


```C++
BOOL fAlreadyInJob;
BOOL fSuccess = IsProcessInJob(GetCurrentProcess(), NULL, &fAlreadyInJob); 
```



Si l’application d’accessibilité est configurée pour s’exécuter en dehors d’un travail, elle doit avertir l’ergonomie du centre d’accès que l’application démarre et se poursuit normalement.

Quelle que soit la façon dont l’application est configurée, si elle offre un moyen de quitter l’application, par exemple un bouton Fermer, l’application doit notifier la facilité d’accès du centre d’accès qu’elle est en cours de fermeture.

une application notifie la facilité d’accès au centre d’accès en définissant une clé de registre temporaire, puis en injectant la combinaison de touches Windows le Logo + U dans le flux d’entrée.

L’application doit créer la clé temporaire à l’emplacement suivant.

**\\logiciel HKCU \\ Microsoft \\ Windows NT \\ CurrentVersion \\ AccessibilityTemp**

La clé temporaire doit avoir le même nom que le nom de l’application inscrite, par exemple « \_ lecteur d’écran Contoso \_ v 1.0 ». La valeur de la clé est un **DWORD** défini sur 0x0003 lors du démarrage ou 0x0002 lorsque l’application est en cours de fermeture.


```C++
INPUT input[4] = {0};

input[0].type = INPUT_KEYBOARD;
input[0].ki.wVk = VK_LWIN;
input[0].ki.dwFlags = 0;

input[1].type = INPUT_KEYBOARD;
input[1].ki.wVk = 0x55; // U key
input[1].ki.dwFlags = 0;

input[2].type = INPUT_KEYBOARD;
input[2].ki.wVk = 0x55; // U key
input[2].ki.dwFlags = KEYEVENTF_KEYUP;

input[3].type = INPUT_KEYBOARD;
input[3].ki.wVk = VK_LWIN;
input[3].ki.dwFlags = KEYEVENTF_KEYUP;

SendInput(ARRAYSIZE(input), input, sizeof(input[0]));
```



### <a name="windows-logo-key--volume-up"></a>Windows Touche de logo + volume vers le haut

lorsque l’utilisateur démarre votre application d’accessibilité en appuyant sur la combinaison de touches Windows Logo + Volume vers le haut (par exemple, sur un appareil tablette), la facilité d’accès passe l’argument de ligne de commande suivant à l’application :

**/hardwarebuttonlaunch**

Votre application peut utiliser cet argument pour déterminer s’il faut démarrer normalement ou ajuster le comportement en conséquence.

### <a name="transferring-secure-desktop-settings"></a>Transfert des paramètres de bureau sécurisés

Si votre application d’accessibilité prend en charge le Bureau sécurisé, vous pouvez utiliser le registre pour copier les paramètres lors de la transition de l’application vers le Bureau sécurisé. La copie des paramètres permet de rendre la transition vers le Bureau sécurisé plus transparente pour l’utilisateur.

Pour copier les paramètres, affectez la valeur 1 à la clé de Registre CopySettingsToLockedDesktop de l’application, puis stockez les paramètres à l’emplacement de Registre suivant.

**\\logiciel HKCU \\ Microsoft \\ Windows NT \\ CurrentVersion \\ accessibility \\ ATConfig\\<AT Key Name>**

La facilité d’accès surveille cet emplacement du Registre pendant que l’application est en cours d’exécution. Quand une transition vers le Bureau sécurisé se produit, le centre d’ergonomie copie les paramètres dans le même emplacement dans la ruche HKCU du Bureau sécurisé. L’application peut ensuite lire les paramètres et reprendre son état.

Votre application d’accessibilité doit écrire ses paramètres à intervalles réguliers ou chaque fois que les valeurs changent. L’écriture des paramètres sur la sortie de l’application ne fonctionnera pas. Si l’application s’exécute dans un travail, elle se termine à la transition en dehors du Bureau sécurisé, avant que le code de sortie ne puisse être exécuté. Si l’application ne s’exécute pas dans un travail, l’application ne se termine pas à la transition à partir du Bureau sécurisé.

### <a name="caution"></a>Attention

Étant donné que les clés de Registre décrites ici sont écrites en mode utilisateur, elles ne sont pas sécurisées. Si votre application d’accessibilité lit le contenu de ces clés, elle doit vérifier soigneusement les données et les utiliser avec précaution. Plus précisément, votre application doit effectuer une vérification des limites sur les valeurs **DWORD** , faire attention aux longueurs de chaîne, ne doit pas lire les noms de dll de plug-in et ne doit pas exécuter de commandes trouvées dans des chaînes.

## <a name="registry-examples"></a>Exemples de Registre

L’exemple suivant montre les valeurs de Registre possibles pour un produit fictif appelé contoso ScreenReader version 2,0, dont le nom localisé est stocké en tant que ressource.

Les valeurs de la table se trouvent sous la clé suivante :

**HKLM \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ accessibility \\ ATs \\ Contoso \_ Screen Reader \_ v 2.0**



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Nom</th>
<th>Type</th>
<th>Données</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ApplicationName</td>
<td>REG_SZ</td>
<td>@% SystemRoot% \system32\ContosoRes.dll,-5020</td>
</tr>
<tr class="even">
<td>Description</td>
<td>REG_SZ</td>
<td>@% SystemRoot% \system32\ContosoRes.dll,-5040</td>
</tr>
<tr class="odd">
<td>Profil</td>
<td>REG_SZ</td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>XML</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>&lt;HCIModel&gt;
   <Accommodation type=&quot;low vision&quot; />
   <Accommodation type=&quot;severe vision&quot; />
   <Accommodation type=&quot;mild cognitive&quot; />
&lt;/HCIModel&gt;</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>SimpleProfile</td>
<td>REG_SZ</td>
<td>ScreenReader</td>
</tr>
<tr class="odd">
<td>Variable startexe</td>
<td>REG_SZ</td>
<td>C:\ContosoTools\Bin\ContosoSR.exe</td>
</tr>
<tr class="even">
<td>StartParams</td>
<td>REG_SZ</td>

</tr>
<tr class="odd">
<td>SecureDesktopAccommodation</td>
<td>REG_SZ</td>
<td>Narrateur</td>
</tr>
</tbody>
</table>



 

Si l’application fournit à la fois un lecteur d’écran et une loupe d’écran dans un exécutable unique, les valeurs du composant de lecteur d’écran peuvent se présenter comme suit :



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Nom</th>
<th>Type</th>
<th>Données</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ApplicationName</td>
<td>REG_SZ</td>
<td>@C:\Program Files\Contoso\Contosores.dll,-30</td>
</tr>
<tr class="even">
<td>Description</td>
<td>REG_SZ</td>
<td>@C:\Program Files\Contoso\Contosores.dll,-32</td>
</tr>
<tr class="odd">
<td>Profil</td>
<td>REG_SZ</td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>XML</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>&lt;HCIModel&gt;
   <Accommodation type=&quot;low vision&quot; />
   <Accommodation type=&quot;severe vision&quot; />
   <Accommodation type=&quot;mild cognitive&quot; />
&lt;/HCIModel&gt;</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>SimpleProfile</td>
<td>REG_SZ</td>
<td>ScreenReader</td>
</tr>
<tr class="odd">
<td>Variable startexe</td>
<td>REG_SZ</td>
<td>C:\Program Files\Contoso\Bin\ContosoSR.exe</td>
</tr>
<tr class="even">
<td>StartParams</td>
<td>REG_SZ</td>
<td>/r</td>
</tr>
</tbody>
</table>



 

Les valeurs du composant loupe se trouvent dans la clé suivante :

**HKLM \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Contosoibility \\ ATs \\ Contoso \_ magnifier \_ v 2.0**



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Nom</th>
<th>Type</th>
<th>Données</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ApplicationName</td>
<td>REG_SZ</td>
<td>@c:\Program Files\Contoso\Contosores.dll,-31</td>
</tr>
<tr class="even">
<td>Description</td>
<td>REG_SZ</td>
<td>@c:\Program Files\Contoso\Contosores.dll,-42</td>
</tr>
<tr class="odd">
<td>Profil</td>
<td>REG_SZ</td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>XML</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>&lt;HCIModel&gt;
   <Accommodation type=&quot;mild vision&quot; />
&lt;/HCIModel&gt;</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>SimpleProfile</td>
<td>REG_SZ</td>
<td>Agrandissement</td>
</tr>
<tr class="odd">
<td>Variable startexe</td>
<td>REG_SZ</td>
<td>c:\Program Files\Contoso\Bin\ContosoSR.exe</td>
</tr>
<tr class="even">
<td>StartParams</td>
<td>REG_SZ</td>
<td>/m</td>
</tr>
</tbody>
</table>



 

 

