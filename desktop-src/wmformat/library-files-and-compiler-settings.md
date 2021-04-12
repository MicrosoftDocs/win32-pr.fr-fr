---
title: Fichiers de bibliothèque et paramètres du compilateur
description: Fichiers de bibliothèque et paramètres du compilateur
ms.assetid: ae043b1e-1d61-4d5a-be98-54f899fa24ed
keywords:
- Windows Media Format SDK, fichiers de bibliothèque
- Windows Media Format SDK, paramètres du compilateur
- Windows Media Format SDK, fichiers d’en-tête
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 079636c8f01decdcfb90e36641e26c62354a7893
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104463870"
---
# <a name="library-files-and-compiler-settings"></a>Fichiers de bibliothèque et paramètres du compilateur

Pour développer une application à l’aide du kit de développement logiciel (SDK) Windows Media format, vous devez utiliser Microsoft Visual C++ version 6,0 ou ultérieure. Les seuls langages de programmation appropriés au développement sont C++ et C.

Le tableau suivant décrit le contenu des différents fichiers d’en-tête inclus dans ce kit de développement logiciel (SDK).



| Fichier d’en-tête                 | Description                                                                                                                                                                                                                                         |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| asferr. h                    | Définit les codes d’erreur relatifs aux opérations de fichier ASF. Cet en-tête est inclus dans WMSDK. h.                                                                                                                                                            |
| drmexternals. h              | Définit des structures, des énumérations et des constantes utilisées pour la gestion des droits numériques (DRM). Incluez cet en-tête lors de l’écriture d’une application qui utilise DRM.                                                                                            |
| dshowasf. h                  | Définit les filtres Microsoft DirectShow QASF. Incluez cet en-tête lors de l’écriture d’une application DirectShow qui crée ou lit des fichiers ASF. Pour plus d’informations, consultez [DirectShow et Windows Media](directshow-and-windows-media.md).               |
| msnetobj. h                  | Définit l’interface [**IRMGetLicense**](irmgetlicense.md) , qui est implémentée dans l’une des bibliothèques Runtime installées avec le kit de développement logiciel (SDK) du format Windows Media.                                                                                     |
| nserror. h                   | Définit les codes d’erreur pour les technologies Windows Media. Seul un sous-ensemble de ces codes d’erreur est pertinent pour le kit de développement logiciel (SDK) du format Windows Media. Cet en-tête est inclus dans WMSDK. h.                                                                            |
| wmdxva. h                    | Comprend d’autres en-têtes et définitions nécessaires pour activer l’accélération vidéo de Microsoft DirectX pour la lecture de contenu Windows Media. Pour plus d’informations, consultez [activation de l’accélération vidéo DirectX](enabling-directx-video-acceleration.md). |
| wmnetsourcecreator. h        | Contient les informations nécessaires à la création de plug-ins source réseau.                                                                                                                                                                                      |
| wmsbuffer. h                 | Définit les interfaces utilisées par les objets de mémoire tampon. Incluez cet en-tête lors de la création de vos propres mémoires tampons pour la lecture de fichiers.                                                                                                                                 |
| WMSDK. h                     | En-tête principal pour les applications qui utilisent le kit de développement logiciel (SDK) Windows Media format. Cet en-tête ne contient aucune définition, mais inclut asferr. h, nserror. h, Windows. h et wmsdkidl. h. Incluez cet en-tête pour toutes les applications utilisant ce kit de développement logiciel.                     |
| wmsdkidl. h                  | Définit les interfaces, fonctions, structures, énumérations et constantes pour la plupart des objets du kit de développement logiciel (SDK) du format Windows Media. Cet en-tête est inclus dans WMSDK. h.                                                                             |
| wmsinternaladminnetsource. h | Définit les interfaces des plug-ins source réseau.                                                                                                                                                                                                  |
| wmsysprf. h                  | Définit les constantes pour les profils système. Incluez cet en-tête dans les applications qui chargent les profils système par identificateur.                                                                                                                         |



 

Pour utiliser le kit de développement logiciel (SDK) Windows Media format, votre compilateur doit être correctement configuré. La configuration est différente pour la génération en mode débogage que pour le mode release. Configurez votre paramètre conformément au tableau suivant. Tous ces paramètres sont configurés dans la boîte de dialogue Paramètres du projet. Pour accéder à la boîte de dialogue, sélectionnez **paramètres** dans le menu **projet** .



| Paramètre                                                                 | Valeur de débogage                                                                              | Valeur de version                                                                           |
|-------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| (Onglet C/C++, Category = génération de code) Utiliser la bibliothèque Runtime            | Déboguer la DLL multithread                                                                  | DLL multithread                                                                       |
| (Onglet lien, catégorie = général) Ignorer toutes les bibliothèques par défaut (case à cocher) | Sélectionnée                                                                                 | Sélectionnée                                                                                |
| (Onglet lien, catégorie = général) Modules objet/bibliothèque                   | Include msvcrtd. lib et Wmvcore.lib.Do ne comprennent pas libc. lib ou aucune variation.<br/> | Include Msvcrt. lib et Wmvcore.lib.Do not include libc. lib ou n’importe quelle variation.<br/> |



 

Si vous utilisez Microsoft Visual Studio .NET, les paramètres ont été modifiés à différents emplacements, comme indiqué dans le tableau suivant. Tous ces paramètres sont configurés dans la boîte de dialogue **pages de propriétés** . Pour accéder à la boîte de dialogue, cliquez avec le bouton droit sur votre projet dans le volet **Explorateur de solutions** et sélectionnez **Propriétés** dans le menu contextuel.



| Paramètre                                                                  | Valeur de débogage                                                                              | Valeur de version                                                                           |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| (Propriétés de configuration/C/C++/génération de code) Bibliothèque Runtime     | DLL de débogage multithread (/MDd)                                                          | DLL multithread (/MD)                                                                |
| (Propriétés de configuration/éditeur de liens/entrée) Dépendances supplémentaires      | Include msvcrtd. lib et Wmvcore.lib.Do ne comprennent pas libc. lib ou aucune variation.<br/> | Include Msvcrt. lib et Wmvcore.lib.Do not include libc. lib ou n’importe quelle variation.<br/> |
| (Propriétés de configuration/éditeur de liens/entrée) Ignorer toutes les bibliothèques par défaut | Oui                                                                                      | Oui                                                                                     |



 

Si vous voulez retarder le chargement de Wmvcore.dll ou de toute autre DLL, utilisez l’option de lien/DELAYLOAD dans Microsoft Visual C++ 6,0 ou des dll à chargement différé dans Microsoft Visual C++ .NET.

En outre, vous devez inclure les répertoires pour les bibliothèques et les en-têtes du kit de développement logiciel (SDK) du format Windows Media. Pour rechercher les paramètres de répertoire pour Visual C++ 6,0, dans le menu **Outils** , cliquez sur **options**, puis sur l’onglet **répertoires** . Lorsque vous utilisez Visual C++ .NET, cliquez sur **options** dans le menu **Outils** , puis sélectionnez projets/Répertoires VC + + dans la liste des options. Ajoutez des répertoires comme indiqué dans le tableau suivant. Si vous avez modifié le répertoire d’installation du kit de développement logiciel (SDK) Windows Media format, votre chemin d’accès sera différent.



| Type de répertoire | Chemin d’accès par défaut                 |
|----------------|------------------------------|
| Fichiers Include  | C : \\ WMSDK \\ WMFSDK11 \\ include |
| Fichiers de bibliothèque  | C : \\ WMSDK \\ WMFSDK11 \\ lib     |



 

Si vous utilisez le kit de développement logiciel (SDK) de plateforme, les chemins d’accès par défaut se présentent comme suit :



| Type de répertoire | Chemin d’accès par défaut                                              |
|----------------|-----------------------------------------------------------|
| Fichiers Include  | C : \\ Program Files \\ Microsoft SDsK \\ Windows \\ v 6.0 \\ include |
| Fichiers de bibliothèque  | C : \\ Program Files \\ Microsoft SDsK \\ Windows \\ v 6.0 \\ lib     |



 

Avant d’appeler l’une des fonctions de création, COM doit être initialisé avec un appel à **CoInitialize** ou **CoinitializeEx**. Le modèle de Threading libre ou le modèle de thread cloisonné peut être utilisé, mais le modèle de thread cloisonné impose des restrictions de Threading sur l’application. Pour plus d’informations sur le modèle COM (Component Object Model) Microsoft, consultez la page COM sur le [site Web de Microsoft](../com/the-component-object-model.md).

**Remarque** Les applications qui lisent ou créent des fichiers protégés par les Rights Management numériques (DRM) requièrent une bibliothèque statique individualisée qui doit être obtenue séparément de Microsoft. Pour plus d’informations, consultez le formulaire Windows Media Licensing sur le [site Web de Microsoft](https://www.microsoft.com/licensing/default). Si vous utilisez la bibliothèque DRM, vous ne devez pas établir de liaison avec wmvcore. lib.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Prise en main**](getting-started.md)
</dt> </dl>

 

