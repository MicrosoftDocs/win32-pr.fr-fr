---
description: il existe plusieurs façons d’utiliser Windows recherche pour interroger l’index.
ms.assetid: 2c161b7f-4e28-4e8a-add6-3c1cda00a622
title: Interrogation de l’index programmatiquement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6390b31f4a1cc01ca723978a5107d5d9a502c4ff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231269"
---
# <a name="querying-the-index-programmatically"></a>Interrogation de l’index programmatiquement

il existe plusieurs façons d’utiliser Windows recherche pour interroger l’index.

Cette section fournit l’infrastructure conceptuelle pour l’interrogation de l’index par programme :

-   [utilisation d’approches SQL et AQS pour interroger l’Index](using-sql-and-aqs-to-query-the-index.md)
-   [Interrogation de l’index avec ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)
-   [Interrogation de l’index avec le protocole search-ms](-search-3x-wds-qryidx-searchms.md)
-   [interrogation de l’Index avec Windows syntaxe de SQL de recherche](-search-sql-windowssearch-entry.md)
-   [Utilisation de la syntaxe de requête avancée par programmation](-search-3x-advancedquerysyntax.md)

> [!Note]  
> compatibilité héritée de Microsoft Windows Desktop Search (WDS) 2x : sur les ordinateurs exécutant Windows XP et versions ultérieures, [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) est déconseillé. au lieu de cela, les développeurs doivent utiliser [**ISearchQueryHelper**](/windows/win32/api/Searchapi/nn-searchapi-isearchqueryhelper) pour obtenir une chaîne de connexion et analyser la requête de l’utilisateur dans langage SQL (SQL), puis interroger la base de données de liaison et d’incorporation d’objets (OLE DB).

 

## <a name="additional-resources"></a>Ressources supplémentaires

-   Pour plus d’informations sur la OLE DB, consultez [OLE DB vue d’ensemble](https://msdn.microsoft.com/library/Cc522830(v=VS.71).aspx)de la programmation. pour plus d’informations sur le Fournisseur de données .NET Framework pour OLE DB, consultez l' [espace de noms System. Data. OleDb](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1).
-   Pour plus d’informations sur l’utilisation des propriétés dans l’interrogation, consultez les rubriques suivantes :
    -   [Système de propriétés](../properties/building-property-handlers.md)
    -   [Propriétés système](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
-   Pour plus d’informations sur la façon de créer et de modifier des dossiers de recherche, consultez [**ISearchFolderItemFactory interface**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory).
-   pour obtenir des forums de discussion et des questions sur les technologies de recherche prises en charge par la communauté, consultez le [Forum MSDN : Windows Desktop search Development](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).
-   Pour télécharger les exemples de code du kit de développement logiciel (SDK) Search :
    -   pour Windows 7 : [Windows des exemples de recherche sur GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch)
    -   pour Windows Vista : [exemples du kit de développement logiciel (SDK) Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)
-   pour télécharger les SDK Windows :
    -   pour Windows 7 : [SDK Windows pour Windows 7 et .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)
    -   pour Windows vista : [SDK Windows pour Windows vista et .NET Framework](https://www.microsoft.com/download/details.aspx?id=31950)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Rechercher dans le Guide de développement](-search-developers-guide-entry-page.md)
</dt> <dt>

[Gestion de l’index](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[extension de l’Index de recherche Windows](-search-3x-wds-extidx-overview.md)
</dt> <dt>

[Extension des ressources linguistiques](extending-language-resources-in-windows-search.md)
</dt> </dl>

 

 
