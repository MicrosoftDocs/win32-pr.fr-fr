---
description: Les clés de Registre peuvent être écrites dans le registre système une fois que tous les composants sélectionnés et leurs fichiers associés ont été installés.
ms.assetid: b3b39471-85b1-4361-94fd-19d0f0ee2b78
title: Modification du Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6ff79ce340b0487c179cb37e44dff9f42e4be8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320386"
---
# <a name="modifying-the-registry"></a><span data-ttu-id="690f2-103">Modification du Registre</span><span class="sxs-lookup"><span data-stu-id="690f2-103">Modifying the Registry</span></span>

<span data-ttu-id="690f2-104">Les clés de Registre peuvent être écrites dans le registre système une fois que tous les composants sélectionnés et leurs fichiers associés ont été installés.</span><span class="sxs-lookup"><span data-stu-id="690f2-104">Registry keys can be written to the system registry once all selected components and their related files have been installed.</span></span> <span data-ttu-id="690f2-105">Les actions standard liées à la modification du Registre doivent être séquencées après les actions standard d’installation de fichier, car les clés de registre ne peuvent pas être écrites, sauf si le composant et le fichier correspondants ont été correctement installés.</span><span class="sxs-lookup"><span data-stu-id="690f2-105">The standard actions related to modifying the registry must be sequenced after the file installation standard actions because registry keys cannot be written unless the corresponding component and file have been successfully installed.</span></span>

<span data-ttu-id="690f2-106">L' [action RegisterClassInfo](registerclassinfo-action.md) accède à la [table de classe](class-table.md) pour enregistrer les informations de classe com des composants installés.</span><span class="sxs-lookup"><span data-stu-id="690f2-106">The [RegisterClassInfo action](registerclassinfo-action.md) accesses the [Class table](class-table.md) to register the COM class information of the installed components.</span></span>

<span data-ttu-id="690f2-107">L' [action RegisterExtensionInfo](registerextensioninfo-action.md) interroge la table d' [extension](extension-table.md) et la [table de verbes](verb-table.md) et enregistre les extensions et les informations de verbe de commande correspondantes auprès du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="690f2-107">The [RegisterExtensionInfo action](registerextensioninfo-action.md) queries the [Extension table](extension-table.md) and [Verb table](verb-table.md) and registers the corresponding extensions and command-verb information with the operating system.</span></span>

<span data-ttu-id="690f2-108">L' [action RegisterProgIdInfo](registerprogidinfo-action.md) gère l’inscription des informations ProgID OLE avec le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="690f2-108">The [RegisterProgIdInfo action](registerprogidinfo-action.md) manages the registration of OLE ProgId information with the operating system.</span></span>

<span data-ttu-id="690f2-109">L' [action RegisterMIMEInfo](registermimeinfo-action.md) traite la [table MIME](mime-table.md) pour inscrire l’association entre un type de contexte MIME, l’extension de nom de fichier et le CLSID.</span><span class="sxs-lookup"><span data-stu-id="690f2-109">The [RegisterMIMEInfo action](registermimeinfo-action.md) processes the [MIME table](mime-table.md) to register the association between a MIME context type, the file name extension, and the CLSID.</span></span>

<span data-ttu-id="690f2-110">L' [action WriteRegistryValues](writeregistryvalues-action.md) traite la [table du registre](registry-table.md) et écrit les clés pour tous les composants qui ont été installés localement ou pour s’exécuter à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="690f2-110">The [WriteRegistryValues action](writeregistryvalues-action.md) processes the [Registry table](registry-table.md) and writes the keys for all components that have been either installed locally or to run from source.</span></span> <span data-ttu-id="690f2-111">La table de registre permet d’écrire des clés dans les ruches **\_ \_ racine de la classe HKEY**, **HKEY \_ Current \_ User**, **HKEY \_ local \_ machine** et **HKEY \_ Users** .</span><span class="sxs-lookup"><span data-stu-id="690f2-111">The Registry table allows keys to be written to the **HKEY\_CLASSES\_ROOT**, **HKEY\_CURRENT\_USER**, **HKEY\_LOCAL\_MACHINE**, and **HKEY\_USERS** registry hives.</span></span>

<span data-ttu-id="690f2-112">L' [action RemoveRegistryValues](removeregistryvalues-action.md) supprime les clés qui ont été marquées pour être supprimées dans la colonne Name de la [table Registry](registry-table.md) ou de la [table RemoveRegistry](removeregistry-table.md).</span><span class="sxs-lookup"><span data-stu-id="690f2-112">The [RemoveRegistryValues action](removeregistryvalues-action.md) removes the keys that have been marked to be deleted in the Name column of the [Registry table](registry-table.md) or the [RemoveRegistry Table](removeregistry-table.md).</span></span>

<span data-ttu-id="690f2-113">L' [action RegisterTypeLibraries](registertypelibraries-action.md) traite la [table Typelib](typelib-table.md) et enregistre les bibliothèques de types installées avec le système.</span><span class="sxs-lookup"><span data-stu-id="690f2-113">The [RegisterTypeLibraries action](registertypelibraries-action.md) processes the [TypeLib table](typelib-table.md) and registers the installed type libraries with the system.</span></span>

 

 



