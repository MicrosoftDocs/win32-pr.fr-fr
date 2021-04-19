---
title: Direct2D ne prend pas en charge le rendu des sous-fichiers enrichis dans Internet Explorer 9
description: Direct2D ne prend pas en charge le rendu des sous-fichiers enrichis dans Internet Explorer 9
ms.assetid: D106FBD6-F05E-41A6-B8F8-569EB9810E2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28f51ae6d098c08c0a18656aae2adf3d79d68652
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314822"
---
# <a name="direct2d-does-not-support-rendering-to-rich-metafiles-in-internet-explorer-9"></a>Direct2D ne prend pas en charge le rendu des sous-fichiers enrichis dans Internet Explorer 9

## <a name="platforms"></a>Plateformes

**Clients** – Windows Vista, Windows 7, Windows 8  
**Serveurs** – windows Server 2008, windows Server 2008 R2, windows server 2012  




## <a name="description"></a>Description

En raison des modifications de rendu internes dans Internet Explorer 9, les API brutes [IHTMLElementRender ::D rawtodc](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85)) et [IViewObject ::D](/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw) créent désormais un métafichier contenant une seule bitmap qui représente le contenu Web au lieu d’un métafichier riche contenant du texte et des informations vectorielles. Cette modification est due au passage du rendu GDI au rendu de Direct2D à accélération matérielle (D2D).

Cette modification affecte les applications qui utilisent ces API et s’appuie sur du texte ou des informations vectorielles dans le métafichier.

## <a name="manifestation"></a>Manifestation

En fonction de l’application affectée par cette modification, les utilisateurs peuvent constater un comportement incorrect ou rompu dans leurs applications.

## <a name="mitigation"></a>Limitation des risques

Les applications qui ont uniquement besoin d’extraire des informations textuelles d’un document Web (sans informations de positionnement) peuvent utiliser la propriété [InnerText](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85)) pour extraire du texte.

Les applications qui utilisent IViewObject ::D RAW peuvent utiliser la [fonctionnalité \_ IVIEWOBJECTDRAW \_ DMLT9 \_ avec \_ ](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85)) la clé de contrôle de fonctionnalité GDI pour revenir au rendu GDI si le mode de document :

-   Est inférieur ou égal à 8
-   Le FCK autorise cet hôte à utiliser GDI
-   Et un contexte de périphérique de métafichier est transmis à l’API

## <a name="resources"></a>Ressources

-   [IHTMLElementRender ::D rawToDC](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85))
-   [IViewObject ::D RAW](/windows/win32/api/oleidl/nf-oleidl-iviewobject-draw)
-   [IHTMLElement :: innerText, propriété](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85))
-   [Contrôles de fonctionnalités Internet (I... Budget](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85))

 

 