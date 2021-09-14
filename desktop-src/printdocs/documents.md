---
description: Cette section décrit les technologies de document prises en charge par Microsoft Windows.
ms.assetid: 14ae2c97-8596-46db-a55c-ef706d2cd00b
title: Documents XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 625c2f04a43db9433fe125b52a4bbc08e37fb4f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293435"
---
# <a name="xps-documents"></a>Documents XPS

Cette section décrit les technologies de document prises en charge par Microsoft Windows.

-   [Choix d’une technologie de document](#choosing-a-document-technology)
-   [Dans cette section](#in-this-section)
-   [Outils de document XPS](#xps-document-tools)
-   [Rubriques connexes](#related-topics)


## <a name="choosing-a-document-technology"></a>Choix d’une technologie de document

Microsoft fournit plusieurs technologies de documents différentes pour prendre en charge une grande variété d’applications de document :

-   **XPS et OpenXPS**

    XPS et OpenXPS sont pris en charge dans Windows 8 et les versions ultérieures de Windows. Consultez le diagramme précédent pour déterminer le scénario d’utilisation approprié pour XPS et OpenXPS. Pour plus d’informations sur ces technologies de documents, consultez [Open XML Paper Specification (en anglais) (OpenXPS)](https://www.ecma-international.org/publications/standards/Ecma-388.htm).

    dans le cas de l’utilisation de OpenXPS avec Windows 8 et Windows Server 2012, la prise en charge est fournie uniquement via l' [API de Document XPS](documents-xps.md)

    Si vous devez effectuer une conversion entre Microsoft XPS (MSXPS) et OpenXPS, Microsoft a fourni un outil (XPSConverter.exe) qui vous permet de convertir des documents au format OpenXPS et vice versa. l’outil fait partie du Kit de pilotes Windows (WDK). Pour télécharger le kit WDK, consultez [Comment obtenir le kit WDK](/windows-hardware/drivers/download-the-wdk).

    pour plus d’informations sur OpenXPS et Windows 8, consultez [prise en charge de OpenXPS dans Windows](/windows-hardware/drivers/print/driver-support-for-openxps).

-   **API de document XPS**

    l’api de Document xps est une api Windows native qui prend en charge le modèle d’objet xps. l’API de Document XPS a été introduite dans Windows 7 et peut être utilisée dans les programmes en mode utilisateur et les pilotes d’imprimante XPSDrv.

    Pour plus d’informations, consultez l’API de document XPS et l' [API de signature numérique XPS](xps-digital-signatures.md).

    \*l’API de Document XPS est également prise en charge dans Windows vista avec Service Pack 2 (SP2) avec la mise à jour de plateforme pour Windows Vista et Windows server 2008 avec sp2 à l’aide de la mise à jour de plateforme pour Windows server 2008. pour plus d’informations sur la mise à jour de plateforme pour Windows vista ou la mise à jour de plateforme pour Windows Server 2008, consultez [mise à jour de plateforme pour Windows vista](/windows/desktop/win7ip/platform-update-for-windows-vista-portal) .

-   **.NET Framework**

    .NET Framework fournit une prise en charge des documents XPS pour les programmes en mode utilisateur et de code géré.

    .NET Framework 3,0 est pris en charge sur Windows XP avec service pack 2 (sp2) et les versions ultérieures de Windows systèmes d’exploitation clients, et sur Windows server 2003 avec service pack 2 (sp2) et versions ultérieures de Windows systèmes d’exploitation serveur.

    .NET Framework 3,5 est pris en charge sur les versions Windows XP de Windows systèmes d’exploitation client et sur Windows server 2003 et versions ultérieures de Windows systèmes d’exploitation serveur.

    > [!Note]  
    > nous recommandons l’utilisation de .NET Framework pour la création de documents XPS dans des applications clientes uniquement, et non dans des applications serveur, à moins que l’application ne se ferme régulièrement, comme c’est le cas pour une application cliente.

     

    pour plus d’informations sur la prise en charge des documents dans .NET Framework, consultez [Windows Presentation Foundation Documents](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).

> [!Note]  
> Pour travailler avec des documents XPS dans un programme, utilisez l’API de document XPS native ou le .NET Framework. l’utilisation simultanée des deux dans le même programme n’est pas prise en charge.

 

## <a name="in-this-section"></a>Dans cette section

cette section décrit les technologies de document Windows natives prises en charge par Microsoft Windows.



| Technologie de document                                                                   | Description                                                                                                                                                                                                                                |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [API de document XPS](documents-xps.md)<br/>                   | Fournit un format fiable pour le papier électronique.<br/> L’API de document XPS décrite dans cette section donne aux programmes et aux pilotes d’impression XPSDrv l’accès au contenu et aux métadonnées d’un document XPS.<br/> |
| [API de signature numérique XPS](xps-digital-signatures.md)<br/> | Active la signature de documents, la vérification de l’identité du signataire et l’indication si un document XPS a été modifié depuis sa signature.<br/>                                                                          |
| [Glossaire de documents XPS](xpsapi-glossary.md)<br/>           | Définitions des termes utilisés par l' [API de document XPS](documents-xps.md) et l' [API de signature numérique XPS](xps-digital-signatures.md).<br/>                                                                              |



 

## <a name="xps-document-tools"></a>Outils de document XPS

Les outils suivants sont disponibles pour vous aider à tester et à résoudre les problèmes liés aux fichiers de document XPS.

-   [IsXPS](/previous-versions/aa348104(v=vs.110))

    Teste la conformité d’un fichier aux spécifications XPS (XML Paper Specification) et OPC (Open Packaging Conventions).

-   [XpsAnalyzer](/windows-hardware/drivers/devtest/xpsanalyzer)

    Outil d’invite de commandes qui analyse les fichiers de document XPS pour la compatibilité avec la spécification XPS 1,0.

-   [PTConform](/previous-versions/dd327476(v=msdn.10))

    Outil qui vérifie la validité des documents PrintTicket et PrintCapabilities.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[API d’impression XPS](./printing-with-the-xpsprint-api.md)
</dt> <dt>

[Packaging](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[Impression](./printdocs-printing.md)
</dt> <dt>
  
[Imprimer un exemple de programme](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208))
</dt> </dl>

 

