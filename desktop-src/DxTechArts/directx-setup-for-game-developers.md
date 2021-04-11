---
title: Installation de DirectX pour les développeurs de jeux
description: Cet article est destiné à répondre à certaines questions courantes sur le runtime DirectX et à l’utilisation de DirectSetup pour installer DirectX.
ms.assetid: 2ab439be-8d99-bcf8-89af-d4274e044c88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9c0faf346bd8793e61a89128ce573e29b7a8267
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031718"
---
# <a name="directx-installation-for-game-developers"></a>Installation de DirectX pour les développeurs de jeux

Cet article est destiné à répondre à certaines questions courantes sur le runtime DirectX et à l’utilisation de DirectSetup pour installer DirectX.

-   [Runtime DirectX](#directx-runtime)
-   [Numéro de version de DirectX](#directx-version-number)
-   [Bibliothèques DirectX](#directx-libraries)
-   [Installation de DirectX par le programme d’installation du jeu](#installation-of-directx-by-the-games-installer)
-   [Petits packages d’installation](#small-installation-packages)
-   [Déploiement interne du runtime DirectX de débogage](#internal-deployment-of-the-debug-directx-runtime)

> [!IMPORTANT]
> Le SDK DirectX hérité est à la fin de la vie, mais il est toujours disponible pour prendre en charge les anciens jeux, didacticiels et projets. Les nouveaux projets ne doivent pas l’utiliser. L’utilisation du SDK DirectX hérité requiert l’utilisation des DirectSetup déconseillés pour les composants tels que D3DX9, D3DX10, D3DX11, XAudio 2,7, XInput 1,3 et XACT. Pour plus d’informations sur l’état actuel du kit de développement logiciel (SDK) DirectX, consultez [où se trouve le kit de développement logiciel (SDK) DirectX](../directx-sdk--august-2009-.md), et le billet de blog [non pour l’installation directe](https://walbourn.github.io/not-so-direct-setup/).

## <a name="directx-runtime"></a>Runtime DirectX

Le composant d’exécution DirectX se compose de composants de base et de composants facultatifs.

Les composants de base, tels que Direct3D et DirectInput, sont considérés comme faisant partie du système d’exploitation. Les composants principaux de DirectX 9.0 c n’ont pas changé depuis la mise à jour 2004 du kit de développement logiciel (SDK) DirectX, et ils correspondent à ce qui a été publié avec Microsoft Windows XP SP2, Windows XP Professionnel Édition x64 et Windows Server 2003 SP1. Windows Vista comprend DirectX 10, qui prend en charge le modèle WDDM (Windows Display Driver Model) et Direct3D 10. x. Windows 7 et Windows Vista (voir [KB971644](https://support.microsoft.com/kb/971644)) prennent en charge DirectX 11, qui prend en charge Direct3D 11, Direct2D, DirectWrite, le périphérique de rendu logiciel WARP10 et les niveaux de fonctionnalité 10level9. Pour plus d’informations, consultez [API graphiques dans Windows](/windows/desktop/direct3darticles/graphics-apis-in-windows-vista) .

Les composants facultatifs sont publiés dans les mises à jour du kit de développement logiciel (SDK) DirectX et incluent D3DX, XACT, XAudio2, XINPUT, Managed DirectX et d’autres composants de ce type. La plupart des composants facultatifs sont régulièrement mis à jour pour intégrer les commentaires des clients et exposer les nouvelles fonctionnalités.

## <a name="directx-version-number"></a>Numéro de version de DirectX

Le numéro de version de DirectX, tel que 9.0 c, fait uniquement référence à la version des composants de base, tels que Direct3D, DirectInput ou DirectSound. Ce nombre ne couvre pas les versions des différents composants facultatifs qui sont publiés dans le kit de développement logiciel (SDK) DirectX, tels que D3DX, XACT, XINPUT, etc.

En règle générale, le numéro de version DirectX n’est pas significatif, sauf en tant que référence rapide aux bits d’exécution de base. Ce nombre ne doit pas être utilisé pour vérifier si le bon runtime DirectX est déjà installé, car il ne prend pas en compte les composants DirectX facultatifs.

## <a name="directx-libraries"></a>Bibliothèques DirectX

Dans le passé, les composants facultatifs du kit de développement logiciel (SDK) DirectX, y compris D3DX, étaient publiés sous forme de bibliothèques statiques. Toutefois, ceux-ci sont désormais publiés en tant que bibliothèques de type dynamique, en raison de l’augmentation de la demande pour de meilleures pratiques de sécurité. Les dll autorisent la maintenance du code précédemment publié. Si ces composants ont été déployés en tant que bibliothèques statiques, Microsoft ne pouvait pas résoudre les problèmes de sécurité détectés après la publication.

À mesure que des fonctionnalités sont ajoutées ou modifiées aux composants facultatifs, les noms des DLL correspondantes sont également modifiés pour garantir qu’aucune régression n’est due aux jeux existants qui utilisent des composants publiés. Les dll pour chaque composant résident côte à côte, et les développeurs de jeux peuvent choisir exactement la version de DLL utilisée par le jeu en établissant un lien avec la bibliothèque d’importation correspondante.

Bien que l’installation des dll sur un système ne soit pas aussi simple que la liaison à des bibliothèques statiques, certaines modifications ont été apportées au kit de développement logiciel (SDK) DirectX pour résoudre les problèmes du modèle de DLL :

-   Le package redistribuable DirectX peut être configuré pour contenir uniquement les composants dont votre application a besoin pour réduire la distribution et la taille des médias.
-   Le dossier redistribuable Program Files \\ SDK du kit de développement logiciel \\ (SDK) DirectX \\ contient maintenant un fichier cabinet (. cab) pour chaque composant facultatif possible. vous n’avez donc pas besoin d’explorer un ancien SDK pour les trouver.
-   L’installation du kit de développement logiciel (SDK) lui-même installe tous les composants facultatifs possibles.
-   Un package redistribuable DirectX qui contient tous les composants facultatifs est disponible à la fois en tant que programme d’installation Web et en tant que package téléchargeable. Pour plus d’informations, consultez le centre de développement DirectX ([DirectX](/previous-versions/windows/apps/hh452744(v=win.10))).

## <a name="installation-of-directx-by-the-games-installer"></a>Installation de DirectX par le programme d’installation du jeu

> [!Note]  
> Consultez [déploiement de Direct3D 11 pour les développeurs de jeux](/windows/desktop/direct3darticles/direct3d11-deployment).

 

Voici les meilleures pratiques pour l’ajout de l’installation de DirectX dans le programme d’installation d’un jeu :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Terme</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Install_the_redistributable_components_every_time.__"></span><span id="install_the_redistributable_components_every_time.__"></span><span id="INSTALL_THE_REDISTRIBUTABLE_COMPONENTS_EVERY_TIME.__"></span>Installez les composants redistribuables à chaque fois. <br/></td>
<td>Le processus d’installation d’un jeu doit installer les composants redistribuables DirectX au cours de chaque installation unique sans permettre aux utilisateurs de le refuser. Si vous autorisez la désactivation, certains utilisateurs devineront qu’ils n’en ont pas besoin et, s’ils le font, le jeu ne s’exécutera pas. <br/></td>
</tr>
<tr class="even">
<td><span id="Let_the_DirectX_installer_check_for_optional_components.__"></span><span id="let_the_directx_installer_check_for_optional_components.__"></span><span id="LET_THE_DIRECTX_INSTALLER_CHECK_FOR_OPTIONAL_COMPONENTS.__"></span>Laissez le programme d’installation DirectX vérifier les composants facultatifs. <br/></td>
<td>Ne partez pas du principe que les derniers composants facultatifs sont déjà installés sur un système, car les Windows Update et les service packs ne fournissent aucun des composants facultatifs de DirectX. Vous devez installer le runtime DirectX en exécutant dxsetup.exe directement ou en appelant DirectSetup. <br/></td>
</tr>
<tr class="odd">
<td><span id="Set_up_silently.__"></span><span id="set_up_silently.__"></span><span id="SET_UP_SILENTLY.__"></span>Configurer en mode silencieux. <br/></td>
<td>Lancez le programme d’installation en mode silencieux afin que les utilisateurs n’ignorent pas accidentellement la mise à jour du runtime DirectX. Pour ce faire, vous pouvez lancer dxsetup.exe à l’aide de la commande suivante : <br/>
<pre class="syntax" data-space="preserve"><code>   path-to-redistributable\dxsetup.exe /silent</code></pre>
ou en appelant DirectSetup et sans aucune interface utilisateur. <br/></td>
</tr>
<tr class="even">
<td><span id="Combine_EULA_acceptances.__"></span><span id="combine_eula_acceptances.__"></span><span id="COMBINE_EULA_ACCEPTANCES.__"></span>Combiner les acceptations du CLUF. <br/></td>
<td>Si vous invitez l’utilisateur à accepter un CLUF, associez-le à l’invite d’acceptation du CLUF DirectX lors de l’installation en mode silencieux afin que l’invitation à accepter les CLUF ne se produise qu’une seule fois. Une invite doit s’afficher avant que vous n’installiez quoi que ce soit si l’utilisateur n’accepte pas, vous ne vous retrouvez pas avec un échec et une installation partielle. <br/></td>
</tr>
<tr class="odd">
<td><span id="Just_run_dxsetup_or_call_DirectSetup.__"></span><span id="just_run_dxsetup_or_call_directsetup.__"></span><span id="JUST_RUN_DXSETUP_OR_CALL_DIRECTSETUP.__"></span>Exécutez simplement Dxsetup ou appelez DirectSetup. <br/></td>
<td>Étant donné que le numéro de version de DirectX ne fait référence à aucun des composants de base DirectX, ne cochez pas une version installée avant d’exécuter dxsetup.exe ou d’appeler DirectSetup. En outre, ne vérifiez pas l’existence d’un fichier pour tester si un composant facultatif est déjà installé, car cela ne déterminera généralement pas correctement quand un composant existe mais a besoin d’être mis à jour. Toutefois, le package d’installation de DirectX détermine rapidement cela et effectue l’action appropriée. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="small-installation-packages"></a>Petits packages d’installation

Vous pouvez créer des packages d’installation plus petits pour DirectX en éliminant le contenu du dossier redistribuable DirectX jusqu’à l’ensemble minimal de fichiers requis pour que le programme d’installation fonctionne et en conservant les composants supplémentaires que votre jeu utilise.

Selon vos spécifications minimales, vous pouvez même ne pas avoir à inclure les fichiers CAB DirectX 9.0 c de base dans le dossier redistribuable de votre support d’installation. Une grande majorité des installations de Windows XP comportent le Service Pack 2, qui comprend les composants de base de DirectX 9.0 c. l’opération d’installation de DirectX sera donc très rapide et ne nécessitera pas de redémarrage. Le plus petit package qui peut être créé est d’environ 3 Mo et peut être compressé à environ la moitié de cette taille. Un package comme celui-ci contient une version de la DLL D3DX et requiert que DirectX 9.0 c soit déjà présent.

L’ensemble minimal de fichiers requis pour générer un package redistribuable est le fichier suivant, situé dans le dossier du kit de développement logiciel (SDK) DirectX (Program Files \\ DirectX SDK redistribut \\ \) :

-   dxsetup.exe
-   dsetup32.dll
-   dsetup.dll
-   dxupdate.cab

Ajoutez à ces fichiers CAB les composants que vous souhaitez installer. Si vous avez besoin que les utilisateurs de votre application disposent déjà de DirectX 9.0 c, vous n’avez pas besoin d’inclure des DirectX.cab ou des dxnt.cab, qui constituent la plupart des besoins en espace. DirectX.cab est nécessaire uniquement pour Windows 98 et Windows ME. dxnt.cab est nécessaire uniquement pour Windows 2000, Windows XP et Windows XP SP1 ; et dxdllreg \_x86.cab sont uniquement requis pour windows 2000, Windows XP RTM, Windows XP SP1 et Windows Server 2003 RTM. En outre, si vous n’utilisez pas DirectShow ou si vous supposez qu’il est déjà installé, vous pouvez omettre BDA.cab, BDANT.cab et BDAXP.cab.

> [!Note]  
> Vous pouvez supposer que les utilisateurs de votre application disposent déjà de DirectX 9.0 c s’ils ont été installés par une version antérieure de votre application, que vous forcez les utilisateurs à effectuer une mise à jour manuelle via le programme d’installation Web ou que vous supposez qu’ils disposent de Windows XP SP2 ou d’une version ultérieure.

 

Si vous continuez avec cet exemple, si vous utilisez uniquement la version 32 bits de D3DX pour le 2006 avril, vous pouvez ajouter Apr2006 \_ d3dx9 \_ 30 \_x86.cab. Si vous utilisez la version 2006 32 bits 32 bits de XINPUT, vous ajoutez Aug2006 \_ XINPUT \_x86.cab.

Si vous disposez d’une application 64 bits native, vous devez ajouter les \_ versions x64. Toutefois, si vous avez une application 32 bits qui s’exécute sur un système d’exploitation 64 bits, les versions 32 bits des dll fonctionnent.

Vous pouvez ensuite distribuer ce package de fichiers et lancer DirectSetup en mode silencieux ou exécuter dxsetup.exe dans l’interface de commande en mode silencieux. N’oubliez pas de ne pas protéger ce package à l’aide d’une vérification de version des fichiers, et de vous assurer que vos utilisateurs ne peuvent pas refuser l’exécution de l’installation de DirectX. L’un de ces événements crée un processus d’installation de Fallible.

## <a name="internal-deployment-of-the-debug-directx-runtime"></a>Déploiement interne du runtime DirectX de débogage

Les runtimes de débogage des composants DirectX sont installés lors de l’installation du kit de développement logiciel (SDK) DirectX, mais l’installation du kit de développement logiciel (SDK) sur chaque ordinateur de test peut être pénible. Vous devez concevoir votre processus d’installation pour copier les dll du runtime de débogage de Program Files \\ Microsoft DirectX SDK \\ Developer \\ architecture \\ vers Windows \\ system32 \\ ou vers le dossier du jeu.

Toutefois, nous vous recommandons vivement de ne pas simplement copier les dll d’exécution publiées, car il est facile d’oublier de les supprimer du produit final. Au lieu de cela, placez les fichiers d’installation de DirectX dans un dossier partagé et exécutez le programme d’installation en mode silencieux à partir du dossier partagé.

## <a name="desktop-bridge-applications"></a>Applications Desktop Bridge 

Les applications de pont de bureau qui utilisent D3DX9, D3DX10, D3DX11, XAudio 2,7, XInput 1,3 ou XACT doivent télécharger l’infrastructure [Microsoft. DirectX. x86](https://download.microsoft.com/download/c/c/2/cc291a37-2ebd-4ac2-ba5f-4c9124733bf1/UAPSignedBinary_Microsoft.DirectX.x86.appx) ou [Microsoft. DirectX. x64](https://download.microsoft.com/download/c/c/2/cc291a37-2ebd-4ac2-ba5f-4c9124733bf1/UAPSignedBinary_Microsoft.DirectX.x64.appx) pour déployer ces composants côte à côte DirectX SDK existants. Vous pouvez également supprimer toutes les dépendances de ce type &mdash; (consultez le [Guide du développeur pour la version redistribuable de xaudio 2,9](../xaudio2/xaudio2-redistributable.md)et les billets de blog [vivant sans D3DX](https://walbourn.github.io/living-without-d3dx/) et [XInput et Windows 8](https://walbourn.github.io/xinput-and-windows-8/)).