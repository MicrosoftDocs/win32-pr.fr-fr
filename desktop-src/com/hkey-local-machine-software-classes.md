---
title: HKEY_LOCAL_MACHINESOFTWAREClasses
description: Les sous-clés et les valeurs de Registre associées à la \_ clé HKEY local \_ machine \\ Software \\ classes contiennent des informations sur une application qui est nécessaire pour prendre en charge les fonctionnalités com.
ms.assetid: a5b271d6-f445-45df-a8e4-f6e0194ac824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c16fdbc97b32d01af9c96b5670cb5a19c09c89a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675598"
---
# <a name="hkey_local_machinesoftwareclasses"></a><span data-ttu-id="d5985-103">HKEY \_ local \_ machine \\ classes de logiciels \\</span><span class="sxs-lookup"><span data-stu-id="d5985-103">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes</span></span>

<span data-ttu-id="d5985-104">Les sous-clés et les valeurs de Registre associées à la clé **HKEY \_ local \_ machine \\ Software \\ classes** contiennent des informations sur une application qui est nécessaire pour prendre en charge les fonctionnalités com.</span><span class="sxs-lookup"><span data-stu-id="d5985-104">The subkeys and registry values associated with the **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key contain information about an application that is needed to support COM functionality.</span></span> <span data-ttu-id="d5985-105">Ces informations incluent des rubriques telles que des formats de données pris en charge, des informations de compatibilité, des identificateurs de programmation, DCOM et des contrôles.</span><span class="sxs-lookup"><span data-stu-id="d5985-105">This information includes such topics as supported data formats, compatibility information, programmatic identifiers, DCOM, and controls.</span></span>



| <span data-ttu-id="d5985-106">Sous-clé</span><span class="sxs-lookup"><span data-stu-id="d5985-106">Subkey</span></span>                                                                         | <span data-ttu-id="d5985-107">Description</span><span class="sxs-lookup"><span data-stu-id="d5985-107">Description</span></span>                                                                                                       |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5985-108">**AppID**</span><span class="sxs-lookup"><span data-stu-id="d5985-108">**AppID**</span></span>](appid-key.md)                                                     | <span data-ttu-id="d5985-109">Options de configuration pour les applications basées sur COM.</span><span class="sxs-lookup"><span data-stu-id="d5985-109">Configuration options for COM-based applications.</span></span>                                                                 |
| [<span data-ttu-id="d5985-110">**IDENTIFICATEUR**</span><span class="sxs-lookup"><span data-stu-id="d5985-110">**CLSID**</span></span>](clsid-key-hklm.md)                                                | <span data-ttu-id="d5985-111">Options de configuration pour les classes COM.</span><span class="sxs-lookup"><span data-stu-id="d5985-111">Configuration options for COM classes.</span></span>                                                                            |
| [<span data-ttu-id="d5985-112">**Extension de fichier<\_>**</span><span class="sxs-lookup"><span data-stu-id="d5985-112">**<file\_extension>**</span></span>](-file-extension--key.md)                        | <span data-ttu-id="d5985-113">Associe une extension de nom de fichier à un ProgID.</span><span class="sxs-lookup"><span data-stu-id="d5985-113">Associates a file name extension with a ProgID.</span></span>                                                                   |
| [<span data-ttu-id="d5985-114">**FileType**</span><span class="sxs-lookup"><span data-stu-id="d5985-114">**FileType**</span></span>](filetype-key.md)                                               | <span data-ttu-id="d5985-115">Utilisé par [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) pour faire correspondre des modèles à différents octets de fichier dans un fichier non composé.</span><span class="sxs-lookup"><span data-stu-id="d5985-115">Used by [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) to match patterns against various file bytes in a non-compound file.</span></span> |
| [<span data-ttu-id="d5985-116">**Interface**</span><span class="sxs-lookup"><span data-stu-id="d5985-116">**Interface**</span></span>](interface-key.md)                                             | <span data-ttu-id="d5985-117">Associe un nom d’interface à un ID d’interface (IID).</span><span class="sxs-lookup"><span data-stu-id="d5985-117">Associates an interface name with an interface ID (IID).</span></span>                                                          |
| [**<ProgID>**](-progid--key.md)                                         | <span data-ttu-id="d5985-118">Identifie une classe.</span><span class="sxs-lookup"><span data-stu-id="d5985-118">Identifies a class.</span></span> <span data-ttu-id="d5985-119">Notez que le ProgID n’est pas garanti globalement unique, contrairement à un CLSID.</span><span class="sxs-lookup"><span data-stu-id="d5985-119">Note that the ProgID is not guaranteed to be globally unique, unlike a CLSID.</span></span>                 |
| [<span data-ttu-id="d5985-120">**ProgID indépendant de la version<>**</span><span class="sxs-lookup"><span data-stu-id="d5985-120">**<version-independent ProgID>**</span></span>](-version-independent-progid--key.md) | <span data-ttu-id="d5985-121">Utilisé pour déterminer la version la plus récente d’une application d’objet.</span><span class="sxs-lookup"><span data-stu-id="d5985-121">Used to determine the latest version of an object application.</span></span>                                                    |



 

 

 




