---
title: Fonctions appelées par le système
description: Fonctions appelées par le système
ms.assetid: 006ac524-d456-44e9-957b-42a85dc92519
keywords:
- audio multimédia, fonctions ACM
- audio, fonctions ACM
- le gestionnaire de compression audio (ACM), fonctions
- ACM (gestionnaire de compression audio), fonctions
- Fonctions ACM
- fonctions de rappel
- Audio Compression Manager (ACM), fonctions de rappel
- ACM (gestionnaire de compression audio), fonctions de rappel
- procédures de Hook
- procédures relatives aux pilotes
- Audio Compression Manager (ACM), procédures de raccordement
- ACM (gestionnaire de compression audio), procédures de raccordement
- Audio Compression Manager (ACM), procédures relatives aux pilotes
- ACM (gestionnaire de compression audio), procédures relatives aux pilotes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b8a8c3615ae0124d4701f8d37d332e652d8390ef165cec8dc57d881cd328fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678618"
---
# <a name="functions-called-by-the-system"></a>Fonctions appelées par le système

Le système appelle trois types différents de fonctions définies par l’application. Les fonctions de rappel sont des fonctions de votre application que le système appelle en réponse à une demande faite par une application. Les procédures de raccordement aident une application à gérer la personnalisation des boîtes de dialogue. Une procédure de pilote est l’implémentation d’une application de son propre codec, convertisseur ou filtre.

Les fonctions de rappel portent les noms suivants :

-   [**acmDriverEnumCallback**](/windows/win32/api/msacm/nc-msacm-acmdriverenumcb)
-   [**acmFilterEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmfilterenumcb)
-   [**acmFilterTagEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmfiltertagenumcb)
-   [**acmFormatEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmformatenumcb)
-   [**acmFormatTagEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmformattagenumcb)
-   [**acmStreamConvertCallback**](/previous-versions//dd742925(v=vs.85))

La plupart des fonctions d’énumération dans l’ACM utilisent des fonctions de rappel. Par exemple, lorsque vous appelez une fonction d’énumération, l’ACM énumère les éléments en appelant de façon répétée l’application via la fonction de rappel.

Certaines fonctions ne peuvent pas être appelées à partir de ces fonctions de rappel. Les fonctions qui ne peuvent pas être appelées manipulent des structures ACM internes qui sont utilisées par les fonctions d’énumération. Les fonctions suivantes ne doivent pas être appelées à partir d’une fonction de rappel :

-   [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd)
-   [**acmDriverPriority**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority)
-   [**acmDriverRemove**](/windows/desktop/api/Msacm/nf-msacm-acmdriverremove)

Le système appelle les fonctions suivantes pour aider une application à gérer la personnalisation des boîtes de dialogue :

-   [**acmFilterChooseHookProc**](/windows/desktop/api/Msacm/nc-msacm-acmfilterchoosehookproc)
-   [**acmFormatChooseHookProc**](/windows/desktop/api/Msacm/nc-msacm-acmformatchoosehookproc)

La fonction suivante est spécifiée en tant que prototype qui permet à une application d’utiliser un codec, un convertisseur ou un filtre personnalisé. Une fonction conforme à ce prototype peut être passée comme argument à la fonction [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) .

-   [**acmDriverProc**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc)

 

 