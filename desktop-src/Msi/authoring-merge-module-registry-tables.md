---
description: Utilisez les tables de registre des modules de fusion en fonction du type d’informations de registre.
ms.assetid: 091429ff-a8f4-4e1b-929f-1559cd173c3d
title: Création de tables de registre de module de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d10e31ac82d190c87019da5bc77408b58122a523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951763"
---
# <a name="authoring-merge-module-registry-tables"></a><span data-ttu-id="2be64-103">Création de tables de registre de module de fusion</span><span class="sxs-lookup"><span data-stu-id="2be64-103">Authoring Merge Module Registry Tables</span></span>

<span data-ttu-id="2be64-104">Utilisez les tables de registre des modules de fusion en fonction du type d’informations de registre.</span><span class="sxs-lookup"><span data-stu-id="2be64-104">Use Merge Module Registry tables according to the type of registry information.</span></span>

## <a name="typelib-class-appid-progid-extension-verb-or-mime-tables"></a><span data-ttu-id="2be64-105">TypeLib, Class, AppId, ProgId, extension, Verb ou MIME tables</span><span class="sxs-lookup"><span data-stu-id="2be64-105">TypeLib, Class, AppId, ProgId, Extension, Verb, or MIME Tables</span></span>

<span data-ttu-id="2be64-106">Pour les bibliothèques de types, les classes, les extensions et les verbes, créez les informations du Registre dans la [TypeLib](typelib-table.md), la [classe](class-table.md), l' [AppID](appid-table.md), le [ProgID](progid-table.md), l' [extension](extension-table.md), le [verbe](verb-table.md)ou les tables [MIME](mime-table.md) du module de fusion.</span><span class="sxs-lookup"><span data-stu-id="2be64-106">For type libraries, classes, extensions, and verbs, author registry information into the merge module's [TypeLib](typelib-table.md), [Class](class-table.md), [AppId](appid-table.md), [ProgId](progid-table.md), [Extension](extension-table.md), [Verb](verb-table.md), or [MIME](mime-table.md) tables.</span></span> <span data-ttu-id="2be64-107">Si vous utilisez la [table du Registre](registry-table.md) pour ajouter ces informations, Windows 2000 ne peut pas fournir de publication à l’ensemble du système pour ces composants.</span><span class="sxs-lookup"><span data-stu-id="2be64-107">If you use the [Registry table](registry-table.md) to add this information, Windows 2000 cannot provide system-wide advertisement for these components.</span></span>

<span data-ttu-id="2be64-108">Les auteurs de modules de fusion peuvent décider de ne pas s’inscrire à l’aide de la table de classes pour les raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="2be64-108">Merge module authors may decide not to register using the Class table for the following reasons:</span></span>

-   <span data-ttu-id="2be64-109">Pour être inscrit par la table de classe, le fichier doit être le chemin d’accès du keyPath de son composant.</span><span class="sxs-lookup"><span data-stu-id="2be64-109">To be registered by the Class table, the file has to be the KeyPath of its component.</span></span> <span data-ttu-id="2be64-110">Cela peut nécessiter une modification inacceptable de l’Organisation des composants.</span><span class="sxs-lookup"><span data-stu-id="2be64-110">This may require an unacceptable change in the organization of components.</span></span>
-   <span data-ttu-id="2be64-111">Un appel COM peut déclencher une tentative de programme d’installation de réinstaller une classe publiée.</span><span class="sxs-lookup"><span data-stu-id="2be64-111">A COM call may trigger an installer attempt to reinstall an advertised class.</span></span> <span data-ttu-id="2be64-112">Les auteurs peuvent décider de ne pas inscrire une classe à l’aide de la table de classes afin d’éviter de déclencher une réinstallation lorsque l’ordinateur client ne prend pas en charge une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2be64-112">Authors may decide not to register a class using the Class table in order to avoid triggering a reinstallation when the client computer does not support a user interface.</span></span>

## <a name="registry-table"></a><span data-ttu-id="2be64-113">Table du Registre</span><span class="sxs-lookup"><span data-stu-id="2be64-113">Registry Table</span></span>

<span data-ttu-id="2be64-114">Utilisez la table Registry pour ajouter des informations de Registre qui ne peuvent pas être créées dans les tables TypeLib, Class, AppId, ProgId, extension, Verb ou MIME.</span><span class="sxs-lookup"><span data-stu-id="2be64-114">Use the Registry table to add registry information that cannot be authored into the TypeLib, Class, AppId, ProgId, Extension, Verb, or MIME tables.</span></span> <span data-ttu-id="2be64-115">Windows 2000 ne peut pas fournir de publication à l’ensemble du système pour les composants qui utilisent la table du Registre.</span><span class="sxs-lookup"><span data-stu-id="2be64-115">Windows 2000 cannot provide system-wide advertisement for components that use the Registry table.</span></span>

<span data-ttu-id="2be64-116">Lors de la création de la table du Registre, consultez chemins d’accès aux fichiers à l’aide du \[ \# fichier \] ou \[ ! \]Format de fichier plutôt qu’en tant que nom de fichier \[ \] du répertoire.</span><span class="sxs-lookup"><span data-stu-id="2be64-116">When authoring the Registry table, refer to file paths using the \[\#File\] or \[!File\] format rather than as \[Directory\]Filename.</span></span> <span data-ttu-id="2be64-117">Ce dernier format ne prend pas en charge l’installation à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="2be64-117">The latter format does not support run-from-source installation.</span></span> <span data-ttu-id="2be64-118">Le format précédent rend également les fichiers manquants et les composants défectueux plus faciles à détecter.</span><span class="sxs-lookup"><span data-stu-id="2be64-118">The former format also makes missing files and faulty components easier to detect.</span></span>

<span data-ttu-id="2be64-119">Une attention est nécessaire lors de l’utilisation du texte mis en forme dans la colonne clé de la table du Registre.</span><span class="sxs-lookup"><span data-stu-id="2be64-119">Care is needed when using formatted text in the Key column of the Registry table.</span></span> <span data-ttu-id="2be64-120">Étant donné que Windows Installer ne réinstalle pas les composants qui sont déjà installés, l’utilisation du texte mis en forme dans ce champ peut entraîner la suppression des clés de registre lors de la suppression de l’application.</span><span class="sxs-lookup"><span data-stu-id="2be64-120">Because Windows Installer does not reinstall components that are already installed, using formatted text in this field may cause registry keys to be left behind on application removal.</span></span>

## <a name="selfreg-table"></a><span data-ttu-id="2be64-121">Table SelfReg</span><span class="sxs-lookup"><span data-stu-id="2be64-121">SelfReg Table</span></span>

<span data-ttu-id="2be64-122">L’utilisation de la table SelfReg n’est pas recommandée.</span><span class="sxs-lookup"><span data-stu-id="2be64-122">Using the SelfReg table is not recommended.</span></span> <span data-ttu-id="2be64-123">Pour obtenir la liste des raisons pour lesquelles vous n’utilisez pas l’inscription automatique, consultez la [table Selfreg](selfreg-table.md).</span><span class="sxs-lookup"><span data-stu-id="2be64-123">For a list of reasons for not using self-registration, see [SelfReg table](selfreg-table.md).</span></span> <span data-ttu-id="2be64-124">Vous devez utiliser la TypeLib, la classe, l’AppId, le ProgId, l’extension, le verbe et les tables MIME dans la mesure du possible et la table du Registre dans tous les autres cas.</span><span class="sxs-lookup"><span data-stu-id="2be64-124">You should use the TypeLib, Class, AppId, ProgId, Extension, Verb, and MIME tables where possible instead and the Registry table in all other cases.</span></span>

 

 



