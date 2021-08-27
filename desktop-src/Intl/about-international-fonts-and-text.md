---
description: Les rubriques de cette section traitent des fonctionnalités de base des polices internationales.
ms.assetid: a47303b5-f49b-4d6c-b061-9d6475530e83
title: Gestion des polices internationales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d4c44661b234a95abb4d40f2204382b3d074bf1d7c0bb1c68a241345211695f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083049"
---
# <a name="international-font-management"></a>Gestion des polices internationales

Les rubriques de cette section traitent des fonctionnalités de base des polices internationales. Pour obtenir des instructions sur l’utilisation de la technologie de police internationale dans vos applications, consultez [énumération et sélection des polices internationales](using-international-fonts-and-text.md) et [utilisation de MS Shell Dlg et MS Shell Dlg 2](using-ms-shell-dlg-and-ms-shell-dlg-2.md).

## <a name="font-management-infrastructure"></a>Infrastructure de gestion des polices

à partir de Windows 7, l’infrastructure de gestion des polices prend en charge le masquage des polices qui ne sont pas appropriées pour les listes de sélection de polices d’un utilisateur. Les paramètres système par défaut choisissent de masquer automatiquement les polices qui ne sont pas conçues pour la ou les langues d’entrée (claviers) activées sur le système d’exploitation. En outre, les utilisateurs peuvent choisir de masquer manuellement les polices dans le panneau de configuration polices. Cette fonctionnalité signifie que les utilisateurs n’ont plus besoin de faire face à de longues listes de polices inappropriées et sont particulièrement utiles pour les utilisateurs internationaux qui travaillent dans des scripts non-latins.

dans Windows 7, il n’existe aucune api pour interroger directement les polices qui sont masquées, ou pour définir le masquage des polices. Toutefois, cela ne signifie pas que vous ne pouvez pas tirer parti de cette fonctionnalité dans votre application. si vous utilisez l’API Windows [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) (boîte de dialogue commune de police) pour activer la sélection de police aujourd’hui, vous obtiendrez gratuitement le nouveau comportement. le nouveau ruban de Windows Scenic (contrôles de police) introduit dans Windows 7 prend également en charge ce comportement et fournit une autre raison de « rubaniser » vos applications. Pour plus d’informations sur l’utilisation des contrôles de police dans le ruban et **ChooseFont** pour afficher des polices tout en filtrant les polices masquées, veuillez faire référence à l' [énumération et à la sélection des polices internationales](using-international-fonts-and-text.md).

Notez que le masquage des polices affecte uniquement l’interface utilisateur de sélection de polices. Elle n’affecte pas les API de dessin. Quand une police est sélectionnée dans un contexte de périphérique, il n’y a aucun effet sur le dessin en raison de la présence de la police masquée. La fonction [**EnumFontFamiliesEx**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa) continue d’énumérer les polices qui ont la valeur Hidden.

## <a name="gdi-font-embedding-and-subsetting"></a>Incorporation et sous-définition des polices GDI

La technologie des polices internationales utilise la bibliothèque de services d’incorporation de polices pour vous permettre de regrouper des polices TrueType et OpenType dans un document ou un fichier. L’incorporation d’une police dans un fichier garantit que la police sera présente sur l’ordinateur recevant le fichier. Pour plus d’informations, consultez [référence d’incorporation de polices](../gdi/font-embedding-reference.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Énumération et sélection des polices internationales](using-international-fonts-and-text.md)
</dt> <dt>

[Utilisation de MS Shell Dlg et MS Shell Dlg 2](using-ms-shell-dlg-and-ms-shell-dlg-2.md)
</dt> <dt>

[Référence d’incorporation de police](../gdi/font-embedding-reference.md)
</dt> </dl>

 

 
