---
description: Windows fournit aux applications un ensemble complet de fonctions qui permettent l’impression sur différents appareils, tels que les imprimantes laser, les traceurs vectorisés, les imprimantes raster et les télécopieurs.
ms.assetid: e5c115b0-9c1e-46e7-8fb5-eddbc2c75298
title: Impression (documents et impression)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 607e845ffc525701489a53c2a6b4628eceb5840d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522069"
---
# <a name="printing-documents-and-printing"></a>Impression (documents et impression)

Windows fournit aux applications un ensemble complet de fonctions qui permettent l’impression sur différents appareils, tels que les imprimantes laser, les traceurs vectorisés, les imprimantes raster et les télécopieurs.

## <a name="desktop-app-printing"></a>Impression d’applications de bureau

Les programmeurs Windows peuvent choisir parmi plusieurs technologies différentes pour imprimer à partir de leur application.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Technology</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/printdocs/tailored-app-printing-api">API d’impression de package de document</a><br/></td>
<td>Fournit une interface qui permet à une application d’accéder au package de documents d’impression et de le gérer. Cette API est disponible avec Windows 8 et les versions ultérieures de Windows.<br/></td>
</tr>
<tr class="even">
<td><a href="print-spooler-api.md">API du spouleur d’impression</a><br/></td>
<td>Fournit une interface au spouleur d’impression pour permettre aux applications de gérer les imprimantes et les travaux d’impression.<br/> Les applications utilisent l' <a href="print-spooler-api.md">API spouleur d’impression</a> pour démarrer, arrêter, contrôler et configurer les travaux d’impression gérés par le spouleur d’impression, qu’ils utilisent l' <a href="/windows/desktop/printdocs/tailored-app-printing-api">API imprimer le package de document</a> ou l’API d' <a href="gdi-printing.md">impression GDI</a> pour imprimer le contenu.<br/></td>
</tr>
<tr class="odd">
<td><a href="print-ticket-api.md">API ticket d’impression</a><br/></td>
<td>Fournit aux applications des fonctions permettant de gérer et de convertir les tickets d’impression.<br/></td>
</tr>
<tr class="even">
<td><a href="gdi-printing.md">API d’impression GDI</a><br/></td>
<td>Fournit des applications avec une interface d’impression indépendante du périphérique. <br/>
<blockquote>
[!Note]<br />
Les développeurs qui écrivent des applications pour Windows Vista et les versions ultérieures de Windows doivent envisager d’utiliser l' <a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">API de document XPS</a> dans leur application.
</blockquote>
<br/> L' <a href="gdi-printing.md">API d’impression GDI</a> convient aux applications qui doivent s’exécuter sur Windows XP et les versions antérieures de Windows.<br/></td>
</tr>
</tbody>
</table>



 

L’illustration suivante fournit une vue d’ensemble de la façon dont les différentes API d’impression sont liées.

![diagramme qui montre comment une application Windows Native peut utiliser les API d’impression](images/print-apis.png)

 

L' [API d’impression de package de document](./tailored-app-printing-api.md)dans cette section décrit les interfaces imprimer le package de document et aperçu avant impression que vous pouvez utiliser avec Windows 8 et les versions ultérieures de Windows Desktop.

Pour plus d’informations sur l’impression à partir d’applications du Windows Store écrites en JavaScript et HTML, consultez [impression (applications du Windows Store en JavaScript et html)](/previous-versions/windows/apps/hh465225(v=win.10)). Pour plus d’informations sur l’impression à partir d’applications du Windows Store écrites en C#, Microsoft Visual Basic ou C++ et XAML, consultez [impression (applications du Windows Store en C)](/previous-versions/windows/apps/hh465196(v=win.10)).

> [!Note]  
> Pour obtenir la liste des API d’impression d’applications de bureau qui peuvent également être utilisées dans les applications du Windows Store, consultez [Win32 et com pour les applications du Windows Store (impression et documents)](/uwp/win32-and-com/win32-and-com-for-uwp-apps) .

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[API de document XPS](/previous-versions/windows/desktop/dd316976(v=vs.85))
</dt> <dt>

[Communications d’imprimante bidirectionnelles (Centre de développement matériel)](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>

