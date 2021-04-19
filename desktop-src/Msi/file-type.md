---
description: Le type de fichier de type sémantique est l’un des types de format de clé. Ce type se compose d’une clé étrangère dans la table de fichiers fournie par l’utilisateur.
ms.assetid: cbcaa016-879e-48c2-93c6-b0e91e1eb9ed
title: Type de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b47e76f4a910b336c749a4f0d5001c8568cead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543519"
---
# <a name="file-type"></a><span data-ttu-id="1ccb5-104">Type de fichier</span><span class="sxs-lookup"><span data-stu-id="1ccb5-104">File Type</span></span>

<span data-ttu-id="1ccb5-105">Le type de fichier de [type sémantique](semantic-types.md) est l’un des [types de format de clé](key-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="1ccb5-105">The File Type of [semantic type](semantic-types.md) is one of the [Key Format Types](key-format-types.md).</span></span> <span data-ttu-id="1ccb5-106">Ce type se compose d’une clé étrangère dans la [table de fichiers](file-table.md) fournie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1ccb5-106">This type consists of a foreign key into the [File table](file-table.md) provided by the user.</span></span>

<span data-ttu-id="1ccb5-107">Le type de fichier peut être utilisé avec les types de ContextData suivants.</span><span class="sxs-lookup"><span data-stu-id="1ccb5-107">The File type may be used with the following kinds of ContextData.</span></span>

<span data-ttu-id="1ccb5-108">**AssemblyContext ContextData**</span><span class="sxs-lookup"><span data-stu-id="1ccb5-108">**AssemblyContext ContextData**</span></span>

<span data-ttu-id="1ccb5-109">Ce type peut être utilisé pour permettre aux utilisateurs de configurer des clés étrangères sur des assemblys Win32 ou common language runtime.</span><span class="sxs-lookup"><span data-stu-id="1ccb5-109">This type may be used to enable users to configure foreign keys to Win32 or common language runtime assemblies.</span></span> <span data-ttu-id="1ccb5-110">L’outil de fusion doit substituer un [identificateur](identifier.md) Windows Installer pour les éléments de ce type dans le modèle dans la colonne valeur de la [table ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="1ccb5-110">The merge tool must substitute a Windows Installer [Identifier](identifier.md) for items of this type into the template in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="1ccb5-111">Mergemod.dll ne l’applique pas et il revient à l’outil de fusion de s’assurer que l’utilisateur fournit une clé valide dans la table de fichiers.</span><span class="sxs-lookup"><span data-stu-id="1ccb5-111">Mergemod.dll does not enforce this and it is up to the merge tool to ensure that the user provides a valid key into the File table.</span></span>

<span data-ttu-id="1ccb5-112">NULL est une valeur valide pour ce type, sauf si msmConfigItemNonNullable a été inclus dans le champ Attributes de la [table ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="1ccb5-112">Null is a valid value for this type unless the msmConfigItemNonNullable has been included in the Attributes field of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

 

 



