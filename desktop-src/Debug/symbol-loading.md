---
description: Le gestionnaire de symboles chargera les symboles quand vous appelez la fonction SymInitialize avec le paramètre fInvadeProcess défini sur TRUE ou lorsque vous appelez la fonction SymLoadModuleEx pour spécifier un module.
ms.assetid: fae1895e-9fed-45e3-8ecf-4c6cc67a6094
title: Chargement de symboles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1459f0fd05b490730739852b77edd29df38c04cbe246699552a53b7e30decf11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912356"
---
# <a name="symbol-loading"></a>Chargement de symboles

Le gestionnaire de symboles chargera les symboles quand vous appelez la fonction [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) avec le paramètre *FInvadeProcess* défini sur **true** ou lorsque vous appelez la fonction [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) pour spécifier un module. Dans les deux cas, le gestionnaire de symboles charge les symboles ou diffère le chargement de symboles jusqu’à ce que les symboles soient demandés, selon les options définies par la fonction [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) .

Le gestionnaire de symboles peut être utilisé pour récupérer des informations symboliques pour n’importe quel module ; elle n’a pas besoin d’être associée à un processus spécifié dans l’appel [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) . Pour utiliser un module arbitraire, spécifiez le chemin d’accès complet à l’image de module dans le paramètre *ImageName* . Vous pouvez utiliser un chemin d’accès à n’importe quel module exécutable contenant des informations de débogage (.exe, .dll,. drv, .sys,. scr, .cpl ou. com). Utilisez le paramètre *BaseOfDll* pour spécifier une adresse de chargement, puis les adresses de symboles seront basées sur cette adresse.

Il n’est peut-être pas nécessaire de garder un module de symboles chargé pendant la durée d’une application. Pour libérer le module de symboles à partir de la liste des modules du gestionnaire de symboles, utilisez la fonction [**SymUnloadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule) . Cette fonction libère la mémoire allouée pour le module de symboles. Pour réutiliser les symboles de ce module, vous devez appeler la fonction [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) même si l’option de chargement différé des symboles est définie.

## <a name="diagnosing-symbol-load-problems"></a>Diagnostic des problèmes de chargement des symboles

Pour afficher toutes les tentatives de chargement de symboles, appelez [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) avec SYMOPT \_ Debug. Cela amène le DbgHelp à appeler la fonction [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) avec des informations détaillées sur les recherches de symboles, telles que les répertoires dans lesquels il recherche et les messages d’erreur. Si votre code utilise [**SymRegisterCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback), dbghelp appellera votre fonction de rappel au lieu d’appeler **OutputDebugString**. Le paramètre *ActionCode* est défini sur cba \_ informations de débogage \_ et le paramètre *CallbackData* est une chaîne qui peut être affichée.

Pour permettre l’affichage de la sortie de débogage dans la console sans modifier votre code source, définissez la \_ variable d’environnement dbghelp DBGOUT sur une valeur non **null** avant d’appeler la fonction [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) . Pour consigner les informations dans un fichier, définissez la \_ variable d’environnement de journalisation dbghelp sur le nom du fichier journal à utiliser.

Notez que ces fonctionnalités doivent être utilisées uniquement lorsque cela est nécessaire. Ils peuvent ralentir le chargement de symboles des modules qui contiennent de nombreux symboles.

 

 
