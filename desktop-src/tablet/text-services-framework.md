---
description: Vue d’ensemble de l’infrastructure de services de texte pour Tablet PC.
ms.assetid: f77fe77a-8625-47c5-bfc7-b473c8e8a8c6
title: Text Services Framework (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f5dca55191518813d6d5680562206f6bc0c72582c905104160a96079087423d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119819799"
---
# <a name="text-services-framework-tablet-pc"></a>Text Services Framework (Tablet PC)

Lorsque [Text Services Framework (TSF)](../tsf/text-services-framework.md) est activé sur un contrôle avec un objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) joint, l’objet PenInputPanel peut insérer du texte directement. Si le contrôle ne prend pas en charge Text Services Framework (TSF), l’objet PenInputPanel doit recourir à l’utilisation de la [fonction SendInput](/windows/win32/api/winuser/nf-winuser-sendinput) pour insérer du texte.

La possibilité d’insérer directement du texte devient très importante pour les caractères d’Extrême-Orient, où l’utilisation de la [fonction SendInput](/windows/win32/api/winuser/nf-winuser-sendinput) peut produire des caractères incorrects.

TSF fournit une interface permettant de corriger les erreurs de reconnaissance, ce qui permet à l’utilisateur final de corriger, de réécrire ou même de dicter le texte approprié.

TSF est activé en appelant la méthode [EnableTsf](/previous-versions/ms569656(v=vs.100)) avec le paramètre *Enable* défini sur **true**.

\[C\#\]


```C++
PenInputPanel thePenInputPanel = new PenInputPanel(theControl);
//...
thePenInputPanel.EnableTsf(true);
```



Un objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) attaché à un contrôle [InkEdit](/previous-versions/ms552265(v=vs.100)) offre une expérience utilisateur robuste, car INKEDIT prend en charge TSF. Toutefois, veillez à définir la propriété [InkMode](/previous-versions/ms835850(v=msdn.10)) sur [Microsoft. Ink. InkMode. Ink](/previous-versions/ms827399(v=msdn.10)) sur le contrôle InkEdit comme indiqué dans la rubrique [meilleures pratiques](best-practices.md) .

L' [exemple PenInputPanel](peninputpanel-sample.md) fournit un exemple d’activation de TSF.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Text Services Framework](../tsf/text-services-framework.md)
</dt> </dl>

 

 
