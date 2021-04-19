---
title: RemoteServerName
description: Configure le client de façon à ce qu’il demande à l’objet d’être exécuté sur un ordinateur particulier chaque fois qu’une fonction d’activation est appelée pour laquelle aucune structure COSERVERINFO n’est spécifiée.
ms.assetid: 0413564e-e8ba-4e6e-ad29-62997c63aab3
keywords:
- Valeur de Registre RemoteServerName COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0634d858b04fbbdf5d3a6024dbd9fdea4ee06d99
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106513560"
---
# <a name="remoteservername"></a><span data-ttu-id="3f318-104">RemoteServerName</span><span class="sxs-lookup"><span data-stu-id="3f318-104">RemoteServerName</span></span>

<span data-ttu-id="3f318-105">Configure le client de façon à ce qu’il demande à l’objet d’être exécuté sur un ordinateur particulier chaque fois qu’une fonction d’activation est appelée pour laquelle aucune structure [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) n’est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3f318-105">Configures the client to request the object be run at a particular computer whenever an activation function is called for which a [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) structure is not specified.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="3f318-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="3f318-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      RemoteServerName = name
```

## <a name="remarks"></a><span data-ttu-id="3f318-107">Notes</span><span class="sxs-lookup"><span data-stu-id="3f318-107">Remarks</span></span>

<span data-ttu-id="3f318-108">**RemoteServerName** permet une gestion de configuration simple des applications clientes ; ils peuvent être écrits sans noms de serveurs codés en dur et peuvent être configurés en modifiant les valeurs de Registre **RemoteServerName** des classes d’objets qu’ils utilisent.</span><span class="sxs-lookup"><span data-stu-id="3f318-108">**RemoteServerName** allows simple configuration management of client applications; they may be written without hard-coded server names and can be configured by modifying the **RemoteServerName** registry values of the classes of objects they use.</span></span>

<span data-ttu-id="3f318-109">Comme décrit dans la documentation de l’énumération [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) et de la structure [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) , l’un des paramètres de l’activation com distribuée est un pointeur vers une structure **COSERVERINFO** .</span><span class="sxs-lookup"><span data-stu-id="3f318-109">As described in the documentation for the [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) enumeration and the [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) structure, one of the parameters of the distributed COM activation is a pointer to a **COSERVERINFO** structure.</span></span> <span data-ttu-id="3f318-110">Lorsque cette valeur n’est pas **null**, les informations contenues dans la structure **COSERVERINFO** remplacent le paramètre de la clé **RemoteServerName** pour l’appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="3f318-110">When this value is not **NULL**, the information in the **COSERVERINFO** structure overrides the setting of the **RemoteServerName** key for the function call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f318-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3f318-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f318-112">Inscription des serveurs COM</span><span class="sxs-lookup"><span data-stu-id="3f318-112">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> </dl>

 

 