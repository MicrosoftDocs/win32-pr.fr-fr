---
description: Ces rubriques décrivent les documents et les fonctionnalités d’impression de Windows qui permettent aux applications d’enregistrer, d’afficher et d’imprimer.
ms.assetid: 20e56af6-9598-4d6a-a2bf-454cef8a3368
title: Documents et impression
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19b23ae7040586d550c47f3fedc59104d83fe818
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106535116"
---
# <a name="documents-and-printing"></a>Documents et impression

Ces rubriques décrivent les documents et les fonctionnalités d’impression de Windows qui permettent aux applications d’enregistrer, d’afficher et d’imprimer.

## <a name="in-this-section"></a>Contenu de cette section



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rubrique</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/printdocs/what-s-new-for-printing-in-windows-vnext">Nouveautés pour l’impression</a><br/></td>
<td>Windows 8 prend en charge <a href="/previous-versions/windows/apps/hh465225(v=win.10)">l’impression pour les applications du Windows Store en JavaScript et html</a> , et <a href="/previous-versions/windows/apps/hh465196(v=win.10)">l’impression pour les applications du Windows Store en C#/VB/C + + et XAML</a>.<br/> Windows 8 inclut également une nouvelle API basée sur COM qui offre une prise en charge complète d’Open XPS et l’accès aux parties des nouveaux pilotes d’imprimante pris en charge par Windows 8. Pour plus d’informations sur la nouvelle API, consultez <a href="/windows/desktop/printdocs/tailored-app-printing-api">Print document package API</a>.<br/> Le programme de boîte de réception du pilote d’impression Windows vérifie que Windows 8 prend en charge un pourcentage élevé des imprimantes populaires.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/printdocs/jobbindalldocuments">Documents XPS</a><br/></td>
<td>Informations sur l’API de document XPS d’une signature numérique XPS.<br/>
<ul>
<li><a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">API de document XPS</a><br/> L’API de document XPS est une API Windows native qui prend en charge le modèle d’objet XPS. L’API de document XPS a été introduite dans Windows 7 et peut être utilisée dans les programmes en mode utilisateur et les pilotes d’imprimante XPSDrv.<br/></li>
<li><a href="/previous-versions/windows/desktop/ff819108(v=vs.85)">API de signature numérique XPS</a><br/> Les signatures numériques XPS activent la signature de documents, la vérification de l’identité du signataire et indiquent si un document XPS a été modifié depuis sa signature.<br/></li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="printdocs-printing.md">Impression</a><br/></td>
<td>Informations sur les fonctionnalités d’impression prises en charge par Windows. Ces fonctionnalités sont les suivantes :<br/>
<ul>
<li><a href="/windows/desktop/printdocs/tailored-app-printing-api">API d’impression de package de document</a><br/> Fournit aux applications une interface qui permet la gestion du package <strong>PrintDocument</strong> .<br/></li>
<li><a href="print-spooler-api.md">API du spouleur d’impression</a><br/> Fournit une interface au spouleur d’impression pour permettre aux applications de gérer les imprimantes et les travaux d’impression.<br/></li>
<li><a href="print-ticket-api.md">API ticket d’impression</a><br/> Fournit aux applications des fonctions permettant de gérer et de convertir les tickets d’impression.<br/></li>
<li><a href="gdi-printing.md">API d’impression GDI</a><br/> Fournit des applications avec une interface d’impression indépendante du périphérique. <br/></li>
<li><p><a href="xps-printing.md">API d’impression XPS</a><br/> Fournit une interface au spouleur d’impression que les applications peuvent utiliser pour envoyer des documents XPS à une imprimante.</p>
<blockquote>
[!Note]<br />
L’API d’impression XPS n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir. Les applications clientes doivent utiliser l' <a href="/windows/desktop/printdocs/tailored-app-printing-api">API Print document package</a> à la place.
</blockquote>
<p><br/> <br/></p></li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/printdocs/printschema">Schéma d’impression</a><br/></td>
<td>Le schéma d’impression et les technologies associées décrivent les fonctionnalités d’une imprimante et spécifient les préférences d’impression d’un document pour les imprimantes et l’affichage des applications. La <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">spécification du schéma d’impression</a> est un document téléchargeable qui contient des informations sur le schéma d’impression et comment l’utiliser dans des documents et l’impression. Les informations en ligne qui se trouvent dans cette section sont fournies uniquement à titre d’information et peuvent ne pas refléter avec précision la version actuelle de la <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">spécification du schéma d’impression</a>.<br/> Reportez-vous à la <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">spécification du schéma d’impression</a> pour obtenir les informations de conception les plus récentes.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="additional-resources"></a>Ressources supplémentaires

L' [exemple d’application Print](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208)) montre comment imprimer à partir d’une application du Windows Store à partir de Windows 8.

Les fonctionnalités décrites dans cette section concernent la programmation Windows native. Pour utiliser des fonctionnalités similaires dans la programmation .NET (managée), consultez [Windows Presentation Foundation des documents](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).

Les documents XPS sont basés sur l’API de [Packaging](/previous-versions/windows/desktop/opc/packaging) . Pour plus d’accès au contenu d’un document XPS, consultez l’API Packaging.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Communications d’imprimante bidirectionnelles (Centre de développement matériel)](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>
