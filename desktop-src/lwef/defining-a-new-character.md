---
title: Définition d’un nouveau caractère
description: Définition d’un nouveau caractère
ms.assetid: 4102cb7d-2fec-45d2-882a-04704c7f5a48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2586312ac9d913a27d2df0be112cbcf92c47f4fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940084"
---
# <a name="defining-a-new-character"></a>Définition d’un nouveau caractère

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Pour définir un nouveau caractère, exécutez l’éditeur de caractères de l’agent. Si vous avez un fichier de caractères existant chargé, choisissez la commande **nouveau** dans le menu **fichier** . Un sous-menu de choix s’affiche. Si vous créez un caractère pour votre propre usage, choisissez **caractère personnalisé**. Si vous souhaitez créer un caractère qui peut être utilisé comme caractère par défaut de l’agent, choisissez **caractère par** défaut. Cela permet de préconfigurer l’éditeur avec tous les noms d’animation et les assignations d’état d’animation requis, ainsi que de définir l’option **prend en charge l’ensemble d’animations standard** . De même, si vous choisissez le caractère Assistant Office, l’éditeur est préconfiguré avec les noms d’animation et l’affectation d’état d’animation requis pour un caractère Assistant Office. Cette action sélectionne l’icône de **caractère** dans l’arborescence et affiche ses pages de propriétés sur le côté droit de la fenêtre. Les sections suivantes décrivent comment définir les propriétés de votre caractère et comment créer des animations pour le caractère.

### <a name="setting-your-characters-general-information"></a>Définition des informations générales de votre caractère

Pour commencer à définir un caractère, entrez le nom du caractère dans la zone de texte **nom** (32 caractères au maximum). Étant donné que Microsoft Agent utilise le nom pour permettre aux utilisateurs d’accéder au caractère, spécifiez un nom convivial. Fournissez un nom qui peut être prononcé à l’aide de l’orthographe conventionnelle, ou vous pouvez désactiver l’entrée vocale pour le caractère. Vous pouvez également spécifier une brève description (256 caractères) de votre caractère dans la zone de texte Description. Le serveur expose ce que vous entrez dans la zone de texte Description aux applications clientes.

Vous pouvez également stocker vos propres données dans le cadre de votre caractère à l’aide du champ ExtraData. Vous pouvez utiliser cette fonctionnalité pour inclure des informations spéciales sur votre caractère ou d’autres données. Une fois compilé avec l’éditeur de caractères, ces informations sont accessibles à l’aide de la propriété ExtraData au moment de l’exécution lorsque le caractère est chargé.

Vous pouvez définir le nom, la description et les informations de données supplémentaires du caractère en fonction du paramètre d’ID de langue du caractère. Pour définir ces données pour une autre langue, sélectionnez langue, puis entrez le texte. Vous devez également avoir installé les pages de codes de langue sur le système pour générer le fichier de caractères. Si vous ne le souhaitez pas, les paramètres de langue appropriés ne sont pas inclus dans le fichier de caractères compilé. Vous n’avez pas besoin de fournir des informations dans d’autres langues. Si ces propriétés sont interrogées au moment de l’exécution à l’aide de l’API de l’agent et qu’il n’existe aucun paramètre spécifique pour cette langue, les paramètres anglais (par défaut) sont retournés.

### <a name="setting-your-characters-output-options"></a>Définition des options de sortie de votre caractère

Si vous définissez l’option prend en charge le jeu d’animations standard, l’éditeur de caractères vérifie que vous avez inclus toutes les animations et les affectations d’état d’animation requises pour un caractère par défaut lorsque vous tentez de générer le caractère. Si un élément est manquant, une boîte de message répertorie les éléments manquants. Pour plus d’informations sur le jeu d’animations standard, consultez [**conception de caractères pour Microsoft Agent**](designing-characters-for-microsoft-agent.md).

Pour la sortie orale de votre caractère, Microsoft agent vous permet de choisir une voix TTS (Text-to-Speech) synthétisée ou une voix utilisant des fichiers audio enregistrés. Si vous souhaitez utiliser une voix synthétisée, activez l’option utiliser la parole synthétisée pour la sortie vocale. Cette opération ajoute une page de voix pour la sélection des caractéristiques de la voix. Choisissez la page voix et utilisez la page contrôles sur cette page pour sélectionner une voix, une vitesse et un ton de tous les moteurs TTS compatibles que vous avez installés. La plage des paramètres vocaux que vous pouvez sélectionner dépend des moteurs TTS. Si vous n’avez pas encore installé de moteur TTS, la liste des ID vocaux est vide. Vous devez avoir un moteur TTS installé avant de définir les paramètres vocaux de votre caractère dans l’éditeur de caractères de l’agent.

Si vous envisagez d’utiliser un moteur TTS pour la sortie de votre caractère, vous devez également installer ce moteur sur le système de l’utilisateur. Si vous sélectionnez une voix basée sur un moteur TTS particulier, mais que l’utilisateur dispose d’un autre moteur TTS installé, le serveur tente de faire correspondre la voix en fonction des caractéristiques que vous avez définies dans l’éditeur de caractères de l’agent.

Si vous envisagez d’utiliser des fichiers audio enregistrés (. Fichiers WAV) pour la sortie orale de votre caractère, vous n’avez pas besoin de vérifier l’option utiliser la parole synthétisée pour la sortie vocale. Au lieu de cela, vous devez enregistrer les fichiers audio de sortie parlé séparément et les charger à partir du code de votre application.

L’option utiliser la **bulle de texte** vous permet de déterminer si vous souhaitez prendre en charge une bulle de mot pour votre caractère. Cette fonctionnalité peut également être définie au moment de l’exécution.

Lorsque l’option **utiliser la bulle de texte** est cochée, vous pouvez accéder à la page de la bulle de **texte** . Les options de la page **bulle de texte** vous permettent de modifier les caractéristiques par défaut de votre bulle de mot. Le paramètre **caractères par ligne** vous permet de définir la largeur de la bulle en fonction du nombre moyen de caractères par ligne. Vous pouvez définir la hauteur par défaut en fonction d’un nombre fixe de lignes que vous souhaitez afficher à la fois ou automatiquement au format texte que vous fournissez dans la méthode [**Speak**](speak-method.md) . Vous pouvez également définir si la bulle est automatiquement masquée après la fin d’une méthode **Speak** et si la bulle affiche ou « place » automatiquement des mots dans le paramètre de vitesse de sortie vocale du caractère.

La page **bulle de mot** vous permet également de définir la police par défaut pour la bulle de texte du caractère et les couleurs d’affichage de l’info-bulle. Toutefois, n’oubliez pas que les utilisateurs peuvent remplacer vos paramètres de police de bulles de mots à l’aide de la feuille de propriétés Microsoft Agent.

### <a name="setting-your-characters-identifier"></a>Définition de l’identificateur de votre caractère

Chaque caractère requiert un identificateur unique (GUID). Le serveur utilise l’identificateur pour différencier les caractères. Lorsque vous créez un caractère, l’éditeur crée automatiquement un nouvel identificateur pour votre caractère. Vous devez modifier l’identificateur d’un caractère uniquement si vous avez copié le fichier de définition de caractères d’un autre caractère ou si vous souhaitez défaire intentionnellement un caractère d’une version précédente. Pour modifier l’identificateur d’un caractère, cliquez sur le bouton nouveau GUID. l’éditeur génère alors un nouvel identificateur.

 

 




