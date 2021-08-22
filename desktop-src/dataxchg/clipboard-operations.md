---
title: Opérations du presse-papiers
description: Une fenêtre doit utiliser le presse-papiers pour couper, copier ou coller des données. Une fenêtre place les données dans le presse-papiers pour les opérations couper et copier et récupère les données du presse-papiers pour les opérations de collage.
ms.assetid: 27f9142c-3154-4de5-aea6-3c53f7e940ec
keywords:
- Windows Interface utilisateur, presse-papiers
- presse-papiers, fenêtres
- presse-papiers, découper des données
- presse-papiers, copier des données
- presse-papiers, coller des données
- presse-papiers, fenêtre propriétaire
- presse-papiers, rendu différé
- presse-papiers, mémoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a0dfe82f6130f0435521ac4e17cf8e8b7162115074f7b3ff716187730f8bb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118545433"
---
# <a name="clipboard-operations"></a>Opérations du presse-papiers

Une fenêtre doit utiliser le presse-papiers pour couper, copier ou coller des données. Une fenêtre place les données dans le presse-papiers pour les opérations couper et copier et récupère les données du presse-papiers pour les opérations de collage. Les sections suivantes décrivent ces opérations et les problèmes connexes.

Pour placer des données dans le presse-papiers ou en extraire des données, une fenêtre doit d’abord ouvrir le presse-papiers à l’aide de la fonction [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) . Le presse-papiers peut être ouvert à la fois dans une seule fenêtre. Pour déterminer dans quelle fenêtre le presse-papiers est ouvert, appelez la fonction [**GetOpenClipboardWindow**](/windows/desktop/api/Winuser/nf-winuser-getopenclipboardwindow) . Une fois l’opération terminée, la fenêtre doit fermer le presse-papiers en appelant la fonction [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) .

Les rubriques suivantes sont présentées dans cette section.

-   [Opérations couper et copier](#cut-and-copy-operations)
-   [Opérations de collage](#paste-operations)
-   [Propriété du presse-papiers](#clipboard-ownership)
-   [Rendu différé](#delayed-rendering)
-   [Mémoire et presse-papiers](#memory-and-the-clipboard)

## <a name="cut-and-copy-operations"></a>Opérations couper et copier

Pour placer des informations dans le presse-papiers, une fenêtre efface d’abord tout contenu du presse-papiers précédent à l’aide de la fonction [**EmptyClipboard**](/windows/win32/api/winuser/nf-winuser-emptyclipboard) . Cette fonction envoie le message [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) au propriétaire du presse-papiers précédent, libère les ressources associées aux données dans le presse-papiers et assigne la propriété du presse-papiers à la fenêtre dans laquelle le presse-papiers est ouvert. Pour savoir quelle fenêtre possède le presse-papiers, appelez la fonction [**GetClipboardOwner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) .

Une fois le presse-papiers vidé, la fenêtre place les données dans le presse-papiers dans autant de formats de presse-papiers que possible, classés du format du presse-papiers le plus descriptif au moins descriptif. Pour chaque format, la fenêtre appelle la fonction [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) , en spécifiant l’identificateur de format et un handle de mémoire globale. Le descripteur de mémoire peut être NULL, ce qui indique que la fenêtre restitue les données à la demande. Pour plus d’informations, consultez [rendu retardé](#delayed-rendering).

## <a name="paste-operations"></a>Opérations de collage

Pour récupérer les informations de collage à partir du presse-papiers, une fenêtre détermine d’abord le format du presse-papiers à récupérer. En règle générale, une fenêtre énumère les formats de presse-papiers disponibles à l’aide de la fonction [**EnumClipboardFormats**](/windows/desktop/api/Winuser/nf-winuser-enumclipboardformats) et utilise le premier format reconnu. Cette méthode sélectionne le meilleur format disponible en fonction de la priorité définie lorsque les données ont été placées dans le presse-papiers.

Une fenêtre peut également utiliser la fonction [**GetPriorityClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-getpriorityclipboardformat) . Cette fonction identifie le meilleur format de presse-papiers disponible en fonction d’une priorité spécifiée. Une fenêtre qui ne reconnaît qu’un seul format de presse-papiers peut simplement déterminer si ce format est disponible à l’aide de la fonction [**IsClipboardFormatAvailable**](/windows/desktop/api/Winuser/nf-winuser-isclipboardformatavailable) .

Une fois que vous avez déterminé le format du presse-papiers à utiliser, une fenêtre appelle la fonction [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) . Cette fonction retourne le descripteur d’un objet mémoire global contenant les données dans le format spécifié. Une fenêtre peut rapidement verrouiller l’objet mémoire afin d’examiner ou de copier les données. Toutefois, une fenêtre ne doit pas libérer l’objet ou la garder verrouillée pendant une longue période de temps.

## <a name="clipboard-ownership"></a>Propriété du presse-papiers

Le *propriétaire du presse-papiers* est la fenêtre associée aux informations contenues dans le presse-papiers. Une fenêtre devient le propriétaire du presse-papiers lorsqu’elle place des données dans le presse-papiers, en particulier quand elle appelle la fonction [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) . La fenêtre reste le propriétaire du presse-papiers jusqu’à ce qu’elle soit fermée ou qu’une autre fenêtre vide le presse-papiers.

Lorsque le presse-papiers est vidé, le propriétaire du presse-papiers reçoit un message [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) . Voici les raisons pour lesquelles une fenêtre peut traiter ce message :

-   La fenêtre a retardé le rendu d’un ou de plusieurs formats de presse-papiers. En réponse au message [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) , la fenêtre peut libérer des ressources allouées pour afficher les données à la demande. Pour plus d’informations sur le rendu des données, consultez [rendu retardé](#delayed-rendering).
-   La fenêtre a placé des données dans le presse-papiers dans un format de presse-papiers privé. Les données des formats de presse-papiers privés ne sont pas libérées par le système lorsque le presse-papiers est vidé. Par conséquent, le propriétaire du presse-papiers doit libérer les données lors de la réception du message [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) . Pour plus d’informations sur les formats de presse-papiers privés, consultez [formats de presse-papiers](clipboard-formats.md).
-   La fenêtre a placé des données dans le presse-papiers à l’aide du format de presse-papiers **CF \_ OWNERDISPLAY** . En réponse au message [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) , la fenêtre peut libérer des ressources utilisées pour afficher des informations dans la fenêtre de la visionneuse du presse-papiers. Pour plus d’informations sur cet autre format, consultez [format d’affichage du propriétaire](about-the-clipboard.md).

## <a name="delayed-rendering"></a>Rendu différé

Quand vous placez un format de presse-papiers dans le presse-papiers, une fenêtre peut retarder le rendu des données dans ce format jusqu’à ce que les données soient nécessaires. Pour ce faire, une application peut spécifier la **valeur null** pour le paramètre *hdata* de la fonction [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) . Cela est utile si l’application prend en charge plusieurs formats de presse-papiers, tout ou partie de ce qui prend du temps à être rendu. En passant un handle **null** , une fenêtre restitue des formats de presse-papiers complexes uniquement quand et si elles sont nécessaires.

Si une fenêtre retarde le rendu d’un format de presse-papiers, elle doit être préparée pour afficher le format à la demande tant qu’il s’agit du propriétaire du presse-papiers. Le système envoie au propriétaire du presse-papiers un message [**WM \_ RENDERFORMAT**](wm-renderformat.md) lorsqu’une demande est reçue pour un format spécifique qui n’a pas été rendu. À la réception de ce message, la fenêtre doit appeler la fonction [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) pour placer un handle de mémoire globale sur le presse-papiers dans le format demandé.

Une application ne doit pas ouvrir le presse-papiers avant d’appeler [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) en réponse au message [**WM \_ RENDERFORMAT**](wm-renderformat.md) . L’ouverture du presse-papiers n’est pas nécessaire, et toute tentative de cette opération échoue car le presse-papiers est actuellement maintenu ouvert par l’application qui a demandé le rendu du format.

Si le propriétaire du presse-papiers va être détruit et qu’il a retardé le rendu de certains ou de tous les formats du presse-papiers, il reçoit le message [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) . À la réception de ce message, la fenêtre doit ouvrir le presse-papiers, vérifier qu’il est toujours le propriétaire du presse-papiers avec la fonction [**GetClipboardOwner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) , puis placer les descripteurs de mémoire valides dans le presse-papiers pour tous les formats de presse-papiers qu’il fournit. Cela permet de s’assurer que ces formats restent disponibles une fois le propriétaire du presse-papiers détruit.

Contrairement à [**WM \_ RENDERFORMAT**](wm-renderformat.md), une application qui répond à [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) doit ouvrir le presse-papiers avant d’appeler [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) pour placer les descripteurs de mémoire globale sur le presse-papiers.

Les formats de presse-papiers qui ne sont pas rendus en réponse au message [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) cessent d’être disponibles pour d’autres applications et ne sont plus énumérés par les fonctions du presse-papiers.

## <a name="memory-and-the-clipboard"></a>Mémoire et presse-papiers

Un objet mémoire qui doit être placé dans le presse-papiers doit être alloué à l’aide de la fonction [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) avec l’indicateur **GMEM \_ MoveOn** .

Une fois qu’un objet mémoire est placé dans le presse-papiers, la propriété de ce descripteur de mémoire est transférée au système. Lorsque le presse-papiers est vidé et que l’objet mémoire a l’un des formats de presse-papiers suivants, le système libère l’objet mémoire en appelant la fonction spécifiée :



| Fonction pour libérer l’objet                             | Format du presse-papiers                                                                                                                                               |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile)<br/> | **CF \_ DSPENHMETAFILE**<br/> **CF \_ DSPMETAFILEPICT**<br/> **CF \_ ENHMETAFILE**<br/> **CF \_ MetaFilePict**<br/>                            |
| [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)<br/>     | **\_bitmap cf**<br/> **CF \_ DSPBITMAP**<br/> **\_palette cf**<br/>                                                                              |
| [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree)<br/>        | **CF \_ DIB**<br/> **CF \_ DIBV5**<br/> **CF \_ DSPTEXT**<br/> **CF \_ OEMTEXT**<br/> **\_texte cf**<br/> **CF \_ UNICODETEXT**<br/>   |
| aucun<br/>                                     | **CF \_ OWNERDISPLAY**<br/> Lorsque le presse-papiers est vidé d’un objet **CF \_ OWNERDISPLAY** , l’application elle-même doit libérer l’objet mémoire.<br/> |



 

 

