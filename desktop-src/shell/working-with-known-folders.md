---
description: Le système de dossiers connu offre un moyen d’interagir avec certains dossiers de profil élevé qui sont présents par défaut dans Windows.
ms.assetid: 8b6163b5-e152-47c2-99f1-43e80cf0713e
title: Utilisation de dossiers connus dans les applications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0981d354e49f569dda229fab32308d8f4a79ff99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484008"
---
# <a name="working-with-known-folders-in-applications"></a>Utilisation de dossiers connus dans les applications

Le système de dossiers connu offre un moyen d’interagir avec certains dossiers de profil élevé qui sont présents par défaut dans Windows. Il autorise également ces mêmes interactions avec les dossiers installés et inscrits auprès du système de dossiers connus par les applications. Cette rubrique traite de ces interactions possibles telles qu’elles sont fournies par les API de dossiers connus.

-   [Interfaces de dossiers connus](#known-folder-interfaces)
-   [Redirection](#redirection)
-   [Rubriques connexes](#related-topics)

> [!IMPORTANT]
> Pour rediriger les documents, les images ou les dossiers de bureau vers OneDrive, utilisez le déplacement de dossiers connu OneDrive au lieu de la méthode de redirection décrite dans cet article. Pour plus d’informations, consultez [Rediriger et déplacer des dossiers connus de Windows vers OneDrive](/onedrive/redirect-known-folders).  

## <a name="known-folder-interfaces"></a>Interfaces de dossiers connus

Il existe deux interfaces de dossier connues : [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) et [**IKnownFolderManager**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager).

[**IKnownFolderManager**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager) fournit de nombreuses fonctions plus générales en ce qui concerne ces dossiers. Ses méthodes vous permettent d’effectuer les opérations suivantes :

-   Récupérez un [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) basé sur le [**KNOWNFOLDERID**](knownfolderid.md)de ce dossier, son nom canonique, son chemin d’accès exprimé sous forme de chaîne ou son chemin d’accès exprimé sous la forme d’un IDList.
-   Convertit un CSIDL en son équivalent [**KNOWNFOLDERID**](knownfolderid.md) ou convertit un **KNOWNFOLDERID** en son équivalent CSIDL hérité.
-   Inscrire ou désinscrire un dossier connu avec le système.
-   Récupérez toutes les valeurs [**KNOWNFOLDERID**](knownfolderid.md) inscrites sur ce système.
-   Rediriger un dossier connu vers un nouvel emplacement.

[**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) fournit une méthode qui permet à un dossier de se rediriger lui-même en fournissant un nouveau chemin d’accès. Ses autres méthodes obtiennent des informations sur un dossier connu spécifique, notamment :

-   Catégorie du dossier : virtuel, fixe, commun ou par utilisateur.
-   Type du dossier, tel que compressé, documents, images ou fichiers utilisateur.
-   [**KNOWNFOLDERID**](knownfolderid.md) du dossier.
-   Chemin d’accès complet du dossier en tant que IDList ou chaîne. Également son chemin d’accès relatif à un dossier parent.
-   Nom canonique du dossier.
-   Info-bulle affichée pour le dossier.
-   Icône affichée pour le dossier.
-   Description du dossier qui explique son rôle et son utilisation.
-   Indique si le dossier peut être redirigé.

[**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) fournit également une méthode pour récupérer un [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) basé sur le dossier. Cela vous permet de lier le dossier à un gestionnaire, de comparer deux dossiers et de récupérer les attributs, le nom complet et le dossier parent du dossier.

## <a name="redirection"></a>Redirection

La redirection de dossiers est une fonctionnalité importante du système de dossiers connu. Tous les dossiers connus de la catégorie [ **Common** KF \_ Category common \_ * *](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category) * * ou [ **par utilisateur** KF \_ Category \_ PerUser * *](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category) * * sont redirigés. Toutefois, le dossier de catégorie [KF **virtuelle** catégorie virtuelle * * * \_ \_ *](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category) ou de catégorie KF fixe [  \_ \_ * * * *](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category)ne peut pas être redirigé.

Les dossiers peuvent être redirigés vers un autre emplacement sur le même ordinateur ou vers un emplacement sur un réseau. Dans le cas d’une redirection de réseau, le dossier peut être mis en cache localement par le biais de la mise en cache côté client pour fournir un accès hors connexion. Toutefois, même en présence d’un cache local, le dossier redirigé lui-même doit être accessible via le réseau.

La redirection de dossiers n’est pas une nouveauté pour Windows Vista. Par exemple, dans Windows XP, certains dossiers identifiés via le système CSIDL peuvent être redirigés par un appel à [**SHSetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetfolderpatha) ou en modifiant l’entrée de CSIDL dans le registre. Dans Windows Vista et versions ultérieures, la redirection doit être effectuée via [**IKnownFolder :: setPath**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-setpath) ou [**SHSetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath).

Pour déterminer si un dossier peut être redirigé, appelez [**IKnownFolder :: GetRedirectionCapabilities**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getredirectioncapabilities). Si le dossier ne peut pas être redirigé, cet appel peut fournir une explication.

Si un dossier est redirigé vers un emplacement réseau, les méthodes [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) peuvent toujours être appelées avec succès.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Dossiers connus, exemple](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))
</dt> </dl>

 

 
