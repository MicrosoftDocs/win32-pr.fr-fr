---
description: Une fois qu’un fichier de symboles a été chargé dans le gestionnaire de symboles, une application peut utiliser les fonctions de localisateur de symboles pour retourner les informations de symbole pour une adresse spécifiée.
ms.assetid: bfc068e1-eced-4ab2-80a3-acc2ed07c841
title: Recherche de symboles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f65830032cf363771b14f779726c59d976e8d30
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104109967"
---
# <a name="finding-symbols"></a>Recherche de symboles

Une fois qu’un fichier de symboles a été chargé dans le gestionnaire de symboles, une application peut utiliser les fonctions de localisateur de symboles pour retourner les informations de symbole pour une adresse spécifiée. Ces fonctions peuvent également rechercher un nom de fichier de code source et un emplacement de numéro de ligne pour une adresse.

## <a name="enumerating-symbol-files"></a>Énumération des fichiers de symboles

Pour récupérer une liste de tous les fichiers de symboles chargés par nom de module, appelez la fonction [**SymEnumerateModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules) . Pour obtenir un exemple, consultez [énumération des modules de symboles](enumerating-symbol-modules.md). Pour récupérer une liste de symboles pour un module donné, appelez la fonction [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) . Pour obtenir un exemple, consultez [énumération de symboles](enumerating-symbols.md).

## <a name="retrieving-symbols-by-address"></a>Récupération de symboles par adresse

Pour récupérer des informations symboliques pour une adresse spécifique, utilisez la fonction [**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) . Cette fonction récupère les informations et les stocke dans une structure d' [**\_ informations de symbole**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) . Étant donné que les noms de symboles sont de longueur variable, vous devez fournir un espace de mémoire tampon supplémentaire à la suite de la déclaration de structure des **\_ informations de symbole** . Pour obtenir un exemple, consultez [récupération des informations de symbole par adresse](retrieving-symbol-information-by-address.md).

Notez que l’adresse n’a pas besoin d’être sur une limite de symboles. Si l’adresse vient après le début d’un symbole mais avant la fin du symbole (le début du symbole plus la taille du symbole), la fonction recherche le symbole.

## <a name="retrieving-symbols-by-symbol-name"></a>Récupération de symboles par nom de symbole

Pour récupérer des informations symboliques dans une structure d' [**\_ informations de symboles**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) pour un module et un nom de symbole spécifiques, utilisez la fonction [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) . Si le chargement de symboles différé est défini, **SymFromName** tente de charger le fichier de symboles pour un module s’il n’a pas déjà été chargé. Pour spécifier un nom de module avec un nom de symbole, utilisez la syntaxe *module*! *SymName*. Le caractère «  ! » délimite le nom du module du nom du symbole. Pour obtenir un exemple, consultez [extraction d’informations de symboles par nom](retrieving-symbol-information-by-name.md).

## <a name="retrieving-line-numbers-by-address"></a>Récupération des numéros de ligne par adresse

Pour récupérer l’emplacement du code source pour une adresse spécifique, utilisez la fonction [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) . Cette fonction remplit une structure [**imagehlp \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) qui comprend le nom du fichier source et l’emplacement du numéro de ligne référencé par l’adresse spécifiée. Pour obtenir un exemple, consultez [récupération des informations de symbole par adresse](retrieving-symbol-information-by-address.md).

## <a name="retrieving-line-numbers-by-symbol-name"></a>Récupération des numéros de ligne par nom de symbole

Pour récupérer l’emplacement du code source d’un nom de symbole spécifique, utilisez la fonction [**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname) . Cette fonction est similaire à [**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname), mais récupère une structure [**imagehlp \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) . Pour utiliser [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) ou **SymGetLineFromName64**, vous devez définir l’option de lignes de charge ( \_ lignes de charge SYMOPT \_ ) à l’aide de la fonction [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) . Pour obtenir un exemple, consultez [extraction d’informations de symboles par nom](retrieving-symbol-information-by-name.md).

 

 



