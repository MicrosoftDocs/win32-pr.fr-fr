---
description: La version de débogage du moteur XAudio2 valide les paramètres et fournit des messages d’avertissement et d’erreur détaillés.
ms.assetid: a7aaebf9-98d4-e96c-993d-b0d0b7074788
title: Fonctionnalités de débogage XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc50e710f30969e024078eeaf2660545e1da45c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752412"
---
# <a name="xaudio2-debugging-facilities"></a><span data-ttu-id="87441-103">Fonctionnalités de débogage XAudio2</span><span class="sxs-lookup"><span data-stu-id="87441-103">XAudio2 Debugging Facilities</span></span>

<span data-ttu-id="87441-104">La version de débogage du moteur XAudio2 valide les paramètres et fournit des messages d’avertissement et d’erreur détaillés.</span><span class="sxs-lookup"><span data-stu-id="87441-104">The debug version of the XAudio2 engine validates parameters, and provides detailed warning and error messages.</span></span>

## <a name="setting-the-debug-logging-level-at-run-time"></a><span data-ttu-id="87441-105">Définition du niveau de journalisation du débogage au moment de l’exécution</span><span class="sxs-lookup"><span data-stu-id="87441-105">Setting the Debug Logging Level at Run Time</span></span>

<span data-ttu-id="87441-106">Vous pouvez définir le niveau des informations de débogage affichées par XAudio2 à tout moment en remplissant une structure [**de \_ \_ configuration de débogage XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration) avec les indicateurs du niveau de journalisation souhaité, puis passer la structure à la méthode [**IXAudio2 :: SetDebugConfiguration**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-setdebugconfiguration) .</span><span class="sxs-lookup"><span data-stu-id="87441-106">You can set the level of debugging information shown by XAudio2 at any time by filling out an [**XAUDIO2\_DEBUG\_CONFIGURATION**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration) structure with the flags for the desired logging level, and then pass the structure to the [**IXAudio2::SetDebugConfiguration**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-setdebugconfiguration) method.</span></span> <span data-ttu-id="87441-107">Les valeurs passées à la méthode **IXAudio2 :: SetDebugConfiguration** remplacent toujours toutes les valeurs par défaut qui ont été définies dans le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="87441-107">Values passed to the **IXAudio2::SetDebugConfiguration** method always override any default values that were set in the Windows registry.</span></span>

## <a name="debug-support"></a><span data-ttu-id="87441-108">Prise en charge du débogage</span><span class="sxs-lookup"><span data-stu-id="87441-108">Debug Support</span></span>

<span data-ttu-id="87441-109">Les fonctionnalités de débogage sont toujours disponibles pour XAUDIO2 dans Windows 8.</span><span class="sxs-lookup"><span data-stu-id="87441-109">The debugging facilities are always available for XAUDIO2 in Windows 8.</span></span>

<span data-ttu-id="87441-110">Pour les versions du kit de développement logiciel (SDK) DirectX de XAUDIO2, vous devez utiliser le **\_ \_ moteur de débogage XAUDIO2** lors de la création de l’objet XAUDIO2 avec [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) et le runtime SDK développeur DirectX doit être installé sur le système pour que le débogage soit pris en charge.</span><span class="sxs-lookup"><span data-stu-id="87441-110">For the DirectX SDK versions of XAUDIO2, you must use **XAUDIO2\_DEBUG\_ENGINE** when creating the XAUDIO2 object with [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) and the system must have the DirectX SDK Developer Runtime installed for debugging to be supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87441-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="87441-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87441-112">Fonctions de débogage</span><span class="sxs-lookup"><span data-stu-id="87441-112">Debugging Facilities</span></span>](debugging-facilities.md)
</dt> <dt>

[<span data-ttu-id="87441-113">Référence de programmation XAudio2</span><span class="sxs-lookup"><span data-stu-id="87441-113">XAudio2 Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 
