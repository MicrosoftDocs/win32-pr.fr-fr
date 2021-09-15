---
title: fichiers de bibliothèque et Paramètres du compilateur
description: fichiers de bibliothèque et Paramètres du compilateur
ms.assetid: ae043b1e-1d61-4d5a-be98-54f899fa24ed
keywords:
- Windows Media Format SDK, fichiers de bibliothèque
- Windows Media Format SDK, paramètres du compilateur
- Windows Media Format SDK, fichiers d’en-tête
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 079636c8f01decdcfb90e36641e26c62354a7893
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295883"
---
# <a name="library-files-and-compiler-settings"></a>fichiers de bibliothèque et Paramètres du compilateur

pour développer une application à l’aide du kit de développement logiciel (SDK) Windows Media Format, vous devez utiliser Microsoft Visual C++ version 6,0 ou ultérieure. Les seuls langages de programmation appropriés au développement sont C++ et C.

Le tableau suivant décrit le contenu des différents fichiers d’en-tête inclus dans ce kit de développement logiciel (SDK).



| Fichier d’en-tête                 | Description                                                                                                                                                                                                                                         |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| asferr. h                    | Définit les codes d’erreur relatifs aux opérations de fichier ASF. Cet en-tête est inclus dans WMSDK. h.                                                                                                                                                            |
| drmexternals. h              | Définit des structures, des énumérations et des constantes utilisées pour la gestion des droits numériques (DRM). Incluez cet en-tête lors de l’écriture d’une application qui utilise DRM.                                                                                            |
| dshowasf. h                  | définit les filtres QASF Microsoft DirectShow. incluez cet en-tête lors de l’écriture d’une application DirectShow qui crée ou lit des fichiers ASF. pour plus d’informations, consultez [DirectShow et Windows Media](directshow-and-windows-media.md).               |
| msnetobj. h                  | définit l’interface [**IRMGetLicense**](irmgetlicense.md) , qui est implémentée dans l’une des bibliothèques runtime installées avec le kit de développement logiciel (SDK) de Format multimédia Windows.                                                                                     |
| nserror. h                   | définit les codes d’erreur pour Windows Technologies multimédias. seul un sous-ensemble de ces codes d’erreur est pertinent pour le kit de développement logiciel (SDK) de Format multimédia Windows. Cet en-tête est inclus dans WMSDK. h.                                                                            |
| wmdxva. h                    | comprend d’autres en-têtes et définitions nécessaires pour activer l’accélération vidéo Microsoft DirectX pour la lecture de contenu multimédia Windows. Pour plus d’informations, consultez [activation de l’accélération vidéo DirectX](enabling-directx-video-acceleration.md). |
| wmnetsourcecreator. h        | Contient les informations nécessaires à la création de plug-ins source réseau.                                                                                                                                                                                      |
| wmsbuffer. h                 | Définit les interfaces utilisées par les objets de mémoire tampon. Incluez cet en-tête lors de la création de vos propres mémoires tampons pour la lecture de fichiers.                                                                                                                                 |
| WMSDK. h                     | en-tête principal pour les applications qui utilisent le kit de développement logiciel (SDK) Windows Media Format. Cet en-tête ne contient aucune définition, mais inclut asferr. h, nserror. h, Windows. h et wmsdkidl. h. Incluez cet en-tête pour toutes les applications utilisant ce kit de développement logiciel.                     |
| wmsdkidl. h                  | définit les interfaces, fonctions, structures, énumérations et constantes pour la plupart des objets du kit de développement logiciel (SDK) de Format multimédia Windows. Cet en-tête est inclus dans WMSDK. h.                                                                             |
| wmsinternaladminnetsource. h | Définit les interfaces des plug-ins source réseau.                                                                                                                                                                                                  |
| wmsysprf. h                  | Définit les constantes pour les profils système. Incluez cet en-tête dans les applications qui chargent les profils système par identificateur.                                                                                                                         |



 

pour utiliser le kit de développement logiciel (SDK) Windows Media Format, votre compilateur doit être correctement configuré. La configuration est différente pour la génération en mode débogage que pour le mode release. Configurez votre paramètre conformément au tableau suivant. tous ces paramètres sont configurés dans la boîte de dialogue Project Paramètres. pour accéder à la boîte de dialogue, sélectionnez **Paramètres** dans le menu **Project** .



| Paramètre                                                                 | Valeur de débogage                                                                              | Valeur de version                                                                           |
|-------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| (Onglet C/C++, Category = génération de code) Utiliser la bibliothèque Runtime            | Déboguer la DLL multithread                                                                  | DLL multithread                                                                       |
| (Onglet lien, catégorie = général) Ignorer toutes les bibliothèques par défaut (case à cocher) | Sélectionnée                                                                                 | Sélectionnée                                                                                |
| (Onglet lien, catégorie = général) Modules objet/bibliothèque                   | Include msvcrtd. lib et Wmvcore.lib.Do ne comprennent pas libc. lib ou aucune variation.<br/> | Include Msvcrt. lib et Wmvcore.lib.Do not include libc. lib ou n’importe quelle variation.<br/> |



 

si vous utilisez Microsoft Visual Studio .net, les paramètres ont été modifiés à différents emplacements, comme indiqué dans le tableau suivant. Tous ces paramètres sont configurés dans la boîte de dialogue **pages de propriétés** . Pour accéder à la boîte de dialogue, cliquez avec le bouton droit sur votre projet dans le volet **Explorateur de solutions** et sélectionnez **Propriétés** dans le menu contextuel.



| Paramètre                                                                  | Valeur de débogage                                                                              | Valeur de version                                                                           |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| (Propriétés de configuration/C/C++/génération de code) Bibliothèque Runtime     | DLL de débogage multithread (/MDd)                                                          | DLL multithread (/MD)                                                                |
| (Propriétés de configuration/éditeur de liens/entrée) Dépendances supplémentaires      | Include msvcrtd. lib et Wmvcore.lib.Do ne comprennent pas libc. lib ou aucune variation.<br/> | Include Msvcrt. lib et Wmvcore.lib.Do not include libc. lib ou n’importe quelle variation.<br/> |
| (Propriétés de configuration/éditeur de liens/entrée) Ignorer toutes les bibliothèques par défaut | Oui                                                                                      | Oui                                                                                     |



 

si vous voulez retarder le chargement de Wmvcore.dll ou de toute autre dll, utilisez l’option de lien/delayload dans Microsoft Visual C++ 6,0 ou des dll à chargement différé dans Microsoft Visual C++ .net.

en outre, vous devez inclure les répertoires pour les bibliothèques et les en-têtes du kit de développement logiciel (SDK) de Format multimédia Windows. Pour rechercher les paramètres de répertoire pour Visual C++ 6,0, dans le menu **Outils** , cliquez sur **options**, puis sur l’onglet **répertoires** . lorsque vous utilisez Visual C++ .net, cliquez sur **Options** dans le menu **outils** , puis sélectionnez projets/répertoires de VC++ dans la liste Options. Ajoutez des répertoires comme indiqué dans le tableau suivant. si vous avez modifié le répertoire d’installation du kit de développement logiciel (SDK) Windows Media Format, votre chemin d’accès sera différent.



| Type de répertoire | Chemin d’accès par défaut                 |
|----------------|------------------------------|
| Fichiers Include  | C : \\ WMSDK \\ WMFSDK11 \\ include |
| Fichiers de bibliothèque  | C : \\ WMSDK \\ WMFSDK11 \\ lib     |



 

Si vous utilisez le kit de développement logiciel (SDK) de plateforme, les chemins d’accès par défaut se présentent comme suit :



| Type de répertoire | Chemin d’accès par défaut                                              |
|----------------|-----------------------------------------------------------|
| Fichiers Include  | C : \\ Program Files \\ Microsoft SDsK \\ Windows \\ v 6.0 \\ include |
| Fichiers de bibliothèque  | C : \\ Program Files \\ Microsoft SDsK \\ Windows \\ v 6.0 \\ Lib     |



 

Avant d’appeler l’une des fonctions de création, COM doit être initialisé avec un appel à **CoInitialize** ou **CoinitializeEx**. Le modèle de Threading libre ou le modèle de thread cloisonné peut être utilisé, mais le modèle de thread cloisonné impose des restrictions de Threading sur l’application. Pour plus d’informations sur le modèle COM (Component Object Model) Microsoft, consultez la page COM sur le [site Web de Microsoft](../com/the-component-object-model.md).

**Remarque** Les applications qui lisent ou créent des fichiers protégés par les Rights Management numériques (DRM) requièrent une bibliothèque statique individualisée qui doit être obtenue séparément de Microsoft. pour plus d’informations, consultez le formulaire de licence multimédia Windows sur le [site Web de Microsoft](https://www.microsoft.com/licensing/default). Si vous utilisez la bibliothèque DRM, vous ne devez pas établir de liaison avec wmvcore. lib.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Prise en main**](getting-started.md)
</dt> </dl>

 

