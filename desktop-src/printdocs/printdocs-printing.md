---
description: Windows fournit aux applications un ensemble complet de fonctions qui permettent l’impression sur différents appareils, tels que les imprimantes laser, les traceurs vectorisés, les imprimantes raster et les télécopieurs.
ms.assetid: e5c115b0-9c1e-46e7-8fb5-eddbc2c75298
title: Impression (documents et impression)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6317275e60346428173bf47bdc8e9f84b7a3e523
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465656"
---
# <a name="printing-documents-and-printing"></a>Impression (documents et impression)

Windows fournit aux applications un ensemble complet de fonctions qui permettent l’impression sur différents appareils, tels que les imprimantes laser, les traceurs vectorisés, les imprimantes raster et les télécopieurs.

## <a name="desktop-app-printing"></a>Impression d’applications de bureau

Windows programmeurs peuvent choisir parmi différentes technologies pour imprimer à partir de leur application.




| Technology | Description | 
|------------|-------------|
| <a href="/windows/desktop/printdocs/tailored-app-printing-api">API d’impression de package de document</a><br /> | Fournit une interface qui permet à une application d’accéder au package de documents d’impression et de le gérer. cette API est disponible avec Windows 8 et les versions ultérieures de Windows.<br /> | 
| <a href="print-spooler-api.md">API du spouleur d’impression</a><br /> | Fournit une interface au spouleur d’impression pour permettre aux applications de gérer les imprimantes et les travaux d’impression.<br /> Les applications utilisent l' <a href="print-spooler-api.md">API spouleur d’impression</a> pour démarrer, arrêter, contrôler et configurer les travaux d’impression gérés par le spouleur d’impression, qu’ils utilisent l' <a href="/windows/desktop/printdocs/tailored-app-printing-api">API imprimer le package de document</a> ou l’API d' <a href="gdi-printing.md">impression GDI</a> pour imprimer le contenu.<br /> | 
| <a href="print-ticket-api.md">API ticket d’impression</a><br /> | Fournit aux applications des fonctions permettant de gérer et de convertir les tickets d’impression.<br /> | 
| <a href="gdi-printing.md">API d’impression GDI</a><br /> | Fournit des applications avec une interface d’impression indépendante du périphérique. <br /><blockquote>[!Note]<br />les développeurs qui écrivent des applications pour Windows Vista et les versions ultérieures de Windows doivent envisager d’utiliser l' <a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">API de Document XPS</a> dans leur application.</blockquote><br /> l' <a href="gdi-printing.md">API d’impression GDI</a> convient aux applications qui doivent s’exécuter sur Windows XP et les versions antérieures de Windows.<br /> | 




 

L’illustration suivante fournit une vue d’ensemble de la façon dont les différentes API d’impression sont liées.

![diagramme qui montre comment une application Windows Native peut utiliser les API d’impression](images/print-apis.png)

 

l' [API d’impression de package de document](./tailored-app-printing-api.md)dans cette section décrit les interfaces imprimer le package de document et aperçu avant impression que vous pouvez utiliser avec Windows 8 et les versions ultérieures de Windows desktop.

pour plus d’informations sur l’impression à partir de Windows applications du windows store écrites en javascript et html, consultez [impression Windows (applications du windows store en javascript et html)](/previous-versions/windows/apps/hh465225(v=win.10)). pour plus d’informations sur l’impression à partir de Windows applications du windows store écrites en C#, Microsoft Visual Basic ou C++ et XAML, consultez [impression (Windows applications du windows store en C)](/previous-versions/windows/apps/hh465196(v=win.10)).

> [!Note]  
> pour obtenir la liste des api d’impression d’applications de bureau qui peuvent également être utilisées Windows dans les applications du windows store, consultez [Win32 et COM pour les applications Windows store (impression et documents)](/uwp/win32-and-com/win32-and-com-for-uwp-apps) .

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[API de document XPS](/previous-versions/windows/desktop/dd316976(v=vs.85))
</dt> <dt>

[communications d’imprimante bidirectionnelles (Centre de développement matériel)](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>

