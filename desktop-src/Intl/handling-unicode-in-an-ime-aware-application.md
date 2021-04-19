---
description: Gestion d’Unicode dans une application IME-Aware
ms.assetid: fa202c1e-d0af-441f-b878-ed98205a880c
title: Gestion d’Unicode dans une application IME-Aware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d78174776eb608c3e494fd5967acba41609e436a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531416"
---
# <a name="handling-unicode-in-an-ime-aware-application"></a><span data-ttu-id="e2c44-103">Gestion d’Unicode dans une application IME-Aware</span><span class="sxs-lookup"><span data-stu-id="e2c44-103">Handling Unicode in an IME-Aware Application</span></span>

<span data-ttu-id="e2c44-104">Deux problèmes sont liés à l’IMM et à sa gestion d’Unicode.</span><span class="sxs-lookup"><span data-stu-id="e2c44-104">Two issues are involved with the IMM and its handling of Unicode.</span></span> <span data-ttu-id="e2c44-105">Le premier problème est que les versions Unicode des fonctions IMM récupèrent la taille d’une mémoire tampon en octets au lieu de caractères Unicode 16 bits.</span><span class="sxs-lookup"><span data-stu-id="e2c44-105">The first issue is that the Unicode versions of IMM functions retrieve the size of a buffer in bytes instead of 16-bit Unicode characters.</span></span> <span data-ttu-id="e2c44-106">Le deuxième problème est que le IMM récupère normalement des caractères Unicode (au lieu de caractères DBCS) dans les messages [**WM \_ char**](../inputdev/wm-char.md) et [**WM \_ IME \_ char**](wm-ime-char.md) .</span><span class="sxs-lookup"><span data-stu-id="e2c44-106">The second issue is that the IMM normally retrieves Unicode characters (instead of DBCS characters) in the [**WM\_CHAR**](../inputdev/wm-char.md) and [**WM\_IME\_CHAR**](wm-ime-char.md) messages.</span></span>

<span data-ttu-id="e2c44-107">Windows prend en charge une interface Unicode pour le IMM, en plus de l’interface ANSI prise en charge à l’origine.</span><span class="sxs-lookup"><span data-stu-id="e2c44-107">Windows supports a Unicode interface for the IMM, in addition to the ANSI interface originally supported.</span></span>

<span data-ttu-id="e2c44-108">Vos applications doivent utiliser [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) pour faire en sorte que les messages [**WM \_ char**](../inputdev/wm-char.md) et [**WM \_ IME \_ char**](wm-ime-char.md) récupèrent des caractères Unicode au lieu de caractères DBCS dans le paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="e2c44-108">Your applications should use [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) to cause the [**WM\_CHAR**](../inputdev/wm-char.md) and [**WM\_IME\_CHAR**](wm-ime-char.md) messages to retrieve Unicode characters instead of DBCS characters in the *wParam* parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2c44-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e2c44-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2c44-110">Utilisation du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="e2c44-110">Using Input Method Manager</span></span>](using-input-method-manager.md)
</dt> </dl>

 

 
