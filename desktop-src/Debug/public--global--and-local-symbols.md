---
description: Les fonctionnalités de gestion des symboles de l’API DbgHelp ont évolué au fil des années.
ms.assetid: 6dc41682-6104-418b-b045-7afe8c2b11e9
title: Symboles publics, globaux et locaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ecaa40549b091af204f2e318aefef8a256408e5f81b461e63a54c333719dd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406099"
---
# <a name="public-global-and-local-symbols"></a>Symboles publics, globaux et locaux

Les fonctionnalités de gestion des symboles de l’API DbgHelp ont évolué au fil des années. Pour vous assurer que votre code fonctionne dans différents scénarios et fournit des détails complets sur les symboles, utilisez les fonctions les plus récentes chaque fois que cela est possible. Par exemple, [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) remplace [**SymEnumerateSymbols64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratesymbols), [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) remplace [**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)et [**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) remplace [**SymGetSymFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromaddr).

## <a name="public-symbols"></a>Symboles publics

Les versions initiales de DbgHelp.dll prises en charge en examinant uniquement les symboles publics. Ces symboles sont générés pour tout élément du code qui doit être exposé entre différents fichiers sources. Ils incluent également tous les éléments qui sont exportés à partir du module.

Les symboles sont soit incorporés dans l’image, soit stockés séparément dans un fichier. dbg ou. pdb. Les seules informations stockées sont le nom et l’adresse du symbole. Les noms sont disponibles sous forme de noms décorés. Pour afficher les noms non décorés, appelez la fonction [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) avec SYMOPT \_ UNDNAME, ou utilisez la fonction [**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname) .

Notez que l’API DbgHelp n’a pas été initialement conçue pour prendre en charge plusieurs instances du même symbole au sein d’un module. Cela est dû au fait que les symboles publics sont limités à des noms uniques au sein d’un module. Par conséquent, [**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname) retourne uniquement le premier symbole qui correspond. Pour récupérer tous les symboles correspondants, appelez [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols).

## <a name="global-and-local-symbols"></a>Symboles globaux et locaux

Les versions plus récentes de DbgHelp.dll prennent en charge les symboles globaux et locaux lors de l’utilisation de fichiers. pdb. Ces nouvelles versions incluent les fonctions statiques, les fonctions étendues dans un fichier source, les paramètres de fonction et les variables locales. Lorsque DbgHelp recherche un symbole, il vérifie les tables de symboles globales et locales avant de vérifier la table de symboles publique. Cela est dû au fait que des informations supplémentaires sont disponibles pour ces types de symboles et qu’elles ne sont disponibles que pour les symboles publics.

Les symboles globaux et locaux sont stockés avec des noms non décorés. Par conséquent, l' \_ indicateur SYMOPT UNDNAME n’a aucun effet. Pour connaître les noms de symboles décorés, vous devez utiliser l' \_ indicateur SYMOPT public \_ only. Cela amène le DbgHelp à rechercher uniquement les symboles publics.

Pour afficher les symboles locaux ou les paramètres de fonction, appelez la fonction [**SymSetContext**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetcontext) avec le membre **InstructionOffset** de la structure de [**\_ \_ Frame de pile imagehlp**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_stack_frame) défini sur l’adresse de n’importe quel symbole de fonction. Les appels suivants à [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) et [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) peuvent fonctionner dans le contexte de cette adresse. Pour ce faire, affectez la **valeur null** au paramètre *BaseOfDll* et omettez le spécificateur de module dans le paramètre *Name* ou *Mask* . Cela force le DbgHelp à rechercher des symboles correspondants dans l’étendue indiquée par **SymSetContext**.

Pour déterminer si un symbole est un paramètre, vérifiez le membre **Flags** de la structure des [**\_ informations de symbole**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) . Si le symbole est un paramètre, le membre contient le \_ paramètre SYMFLAG. S’il s’agit d’un symbole local, le membre contient SYMFLAG \_ local.

 

 



