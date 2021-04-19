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
# <a name="handling-unicode-in-an-ime-aware-application"></a>Gestion d’Unicode dans une application IME-Aware

Deux problèmes sont liés à l’IMM et à sa gestion d’Unicode. Le premier problème est que les versions Unicode des fonctions IMM récupèrent la taille d’une mémoire tampon en octets au lieu de caractères Unicode 16 bits. Le deuxième problème est que le IMM récupère normalement des caractères Unicode (au lieu de caractères DBCS) dans les messages [**WM \_ char**](../inputdev/wm-char.md) et [**WM \_ IME \_ char**](wm-ime-char.md) .

Windows prend en charge une interface Unicode pour le IMM, en plus de l’interface ANSI prise en charge à l’origine.

Vos applications doivent utiliser [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) pour faire en sorte que les messages [**WM \_ char**](../inputdev/wm-char.md) et [**WM \_ IME \_ char**](wm-ime-char.md) récupèrent des caractères Unicode au lieu de caractères DBCS dans le paramètre *wParam* .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du gestionnaire de méthode d’entrée](using-input-method-manager.md)
</dt> </dl>

 

 
