---
description: ces rubriques décrivent les documents et les fonctionnalités d’impression des Windows qui permettent aux applications d’enregistrer, d’afficher et d’imprimer.
ms.assetid: 20e56af6-9598-4d6a-a2bf-454cef8a3368
title: Documents et impression
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87d7af92af0615dcb11d2623be8f2e21ae813aa1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196727"
---
# <a name="documents-and-printing"></a>Documents et impression

ces rubriques décrivent les documents et les fonctionnalités d’impression des Windows qui permettent aux applications d’enregistrer, d’afficher et d’imprimer.

## <a name="in-this-section"></a>Contenu de cette section




| Rubrique | Description | 
|-------|-------------|
| <a href="/windows/desktop/printdocs/what-s-new-for-printing-in-windows-vnext">Nouveautés pour l’impression</a><br /> | Windows 8 prend en charge <a href="/previous-versions/windows/apps/hh465225(v=win.10)">l’impression pour Windows les applications du windows store en JavaScript et HTML</a> et <a href="/previous-versions/windows/apps/hh465196(v=win.10)">l’impression pour Windows les applications du windows store en C#/VB/c + + et XAML</a>.<br /> Windows 8 inclut également une nouvelle API COM qui offre une prise en charge complète d’Open XPS et l’accès aux parties des nouveaux pilotes d’imprimante pris en charge par Windows 8. Pour plus d’informations sur la nouvelle API, consultez <a href="/windows/desktop/printdocs/tailored-app-printing-api">Print document package API</a>.<br /> le programme de boîte de réception du pilote d’impression Windows permet de s’assurer que Windows 8 prend en charge un pourcentage élevé des imprimantes populaires.<br /> | 
| <a href="/windows/desktop/printdocs/jobbindalldocuments">Documents XPS</a><br /> | Informations sur l’API de document XPS d’une signature numérique XPS.<br /><ul><li><a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">API de document XPS</a><br /> l’api de Document xps est une api Windows native qui prend en charge le modèle d’objet xps. l’API de Document XPS a été introduite dans Windows 7 et peut être utilisée dans les programmes en mode utilisateur et les pilotes d’imprimante XPSDrv.<br /></li><li><a href="/previous-versions/windows/desktop/ff819108(v=vs.85)">API de signature numérique XPS</a><br /> Les signatures numériques XPS activent la signature de documents, la vérification de l’identité du signataire et indiquent si un document XPS a été modifié depuis sa signature.<br /></li></ul> | 
| <a href="printdocs-printing.md">Impression</a><br /> | Informations sur les fonctionnalités d’impression prises en charge par Windows. Ces fonctionnalités sont les suivantes :<br /><ul><li><a href="/windows/desktop/printdocs/tailored-app-printing-api">API d’impression de package de document</a><br /> Fournit aux applications une interface qui permet la gestion du package <strong>PrintDocument</strong> .<br /></li><li><a href="print-spooler-api.md">API du spouleur d’impression</a><br /> Fournit une interface au spouleur d’impression pour permettre aux applications de gérer les imprimantes et les travaux d’impression.<br /></li><li><a href="print-ticket-api.md">API ticket d’impression</a><br /> Fournit aux applications des fonctions permettant de gérer et de convertir les tickets d’impression.<br /></li><li><a href="gdi-printing.md">API d’impression GDI</a><br /> Fournit des applications avec une interface d’impression indépendante du périphérique. <br /></li><li><p><a href="xps-printing.md">API d’impression XPS</a><br /> Fournit une interface au spouleur d’impression que les applications peuvent utiliser pour envoyer des documents XPS à une imprimante.</p><blockquote>[!Note]<br />L’API d’impression XPS n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir. Les applications clientes doivent utiliser l' <a href="/windows/desktop/printdocs/tailored-app-printing-api">API Print document package</a> à la place.</blockquote><p><br /><br /></p></li></ul> | 
| <a href="/windows/desktop/printdocs/printschema">Schéma d’impression</a><br /> | Le schéma d’impression et les technologies associées décrivent les fonctionnalités d’une imprimante et spécifient les préférences d’impression d’un document pour les imprimantes et l’affichage des applications. La <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">spécification du schéma d’impression</a> est un document téléchargeable qui contient des informations sur le schéma d’impression et comment l’utiliser dans des documents et l’impression. Les informations en ligne qui se trouvent dans cette section sont fournies uniquement à titre d’information et peuvent ne pas refléter avec précision la version actuelle de la <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">spécification du schéma d’impression</a>.<br /> Reportez-vous à la <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">spécification du schéma d’impression</a> pour obtenir les informations de conception les plus récentes.<br /> | 




 

## <a name="additional-resources"></a>Ressources supplémentaires

l' [exemple d’application print](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208)) montre comment imprimer à partir d’une application Windows Store à partir de Windows 8.

les fonctionnalités décrites dans cette section concernent la programmation Windows native. pour utiliser des fonctionnalités similaires dans la programmation .net (managée), consultez [Windows Presentation Foundation des Documents](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).

Les documents XPS sont basés sur l’API de [Packaging](/previous-versions/windows/desktop/opc/packaging) . Pour plus d’accès au contenu d’un document XPS, consultez l’API Packaging.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[communications d’imprimante bidirectionnelles (Centre de développement matériel)](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>
