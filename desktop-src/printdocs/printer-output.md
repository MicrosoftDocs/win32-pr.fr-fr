---
description: Tout comme une application nécessite un contexte de périphérique (DC) d’affichage avant de pouvoir commencer à dessiner dans la zone cliente d’une fenêtre, elle a besoin d’un contrôleur de domaine d’imprimante avant de pouvoir commencer à envoyer la sortie vers une imprimante.
ms.assetid: 5bdcec28-e28d-402d-8d80-e8aa5ecb4e74
title: Contextes de périphérique d’impression (documents et impression)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c868d5bf8247375375b33bcb034a70bd6f28c5b9104b61e264543a63281069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947399"
---
# <a name="printer-device-contexts-documents-and-printing"></a>Contextes de périphérique d’impression (documents et impression)

Tout comme une application nécessite un contexte de périphérique (DC) d’affichage avant de pouvoir commencer à dessiner dans la zone cliente d’une fenêtre, elle a besoin d’un contrôleur de domaine d’imprimante avant de pouvoir commencer à envoyer la sortie vers une imprimante. Un contrôleur de service d’imprimante est similaire à un DC d’affichage, car il s’agit d’une structure de données interne qui définit un ensemble d’objets graphiques et leurs attributs associés et spécifie les modes graphiques qui affectent la sortie. Les objets graphiques incluent un stylet pour le dessin de ligne, un pinceau pour la peinture et le remplissage et une police pour la sortie de texte.

Contrairement à un contrôleur de périphérique d’affichage, un contrôleur de périphérique d’imprimante n’est pas détenu par le composant de gestion de fenêtre et il ne peut pas être obtenu en appelant la fonction [**GetDC**](/windows/desktop/api/winuser/nf-winuser-getdc) . Au lieu de cela, une application doit appeler la fonction [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) ou [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) .

Si votre application appelle la fonction [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) , elle doit fournir un nom de pilote et de port. Pour récupérer ces noms, appelez la fonction [**GetPrinter**](getprinter.md) ou [**EnumPrinters**](enumprinters.md) .

Si votre application appelle la fonction [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) et spécifie la \_ valeur PD RETURNDC dans le membre **Flags** de la structure [**PrintDlgEx**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) , le système retourne un handle vers un contexte de périphérique pour l’imprimante sélectionnée par l’utilisateur. Pour plus d’informations, consultez [imprimer la feuille de propriétés](../dlgbox/print-property-sheet.md) et « utilisation de la feuille de propriétés d’impression » dans utilisation des boîtes de [dialogue courantes](../dlgbox/using-common-dialog-boxes.md).

 

 
