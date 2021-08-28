---
description: Fonctions de sortie de débogage
ms.assetid: dfe44c8c-43ec-461f-952f-b87256b82ee6
title: Fonctions de sortie de débogage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee1bdbc9cce98ce1704b62a8354b81951df33c4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884240"
---
# <a name="debug-output-functions"></a>Fonctions de sortie de débogage

les [Classes de Base DirectShow](directshow-base-classes.md) fournissent plusieurs macros pour l’affichage des informations de débogage.



| Fonction                                               | Description                                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DbgCheckModuleLevel**](dbgcheckmodulelevel.md)     | Vérifie si la journalisation est activée pour les types de messages et le niveau donnés.                             |
| [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) | Affiche des informations sur les objets actifs.                                                           |
| [**DbgInitialise**](dbginitialise.md)                 | Initialise la bibliothèque de débogage.                                                                       |
| [**DbgLog**](dbglog.md)                               | Envoie une chaîne à l’emplacement de sortie de débogage, si la journalisation est activée pour le type et le niveau spécifiés. |
| [**DbgOutString**](dbgoutstring.md)                   | Envoie une chaîne à l’emplacement de sortie de débogage.                                                         |
| [**DbgSetModuleLevel**](dbgsetmodulelevel.md)         | Définit le niveau de journalisation pour un ou plusieurs types de messages.                                                |
| [**DbgTerminate**](dbgterminate.md)                   | Nettoie la bibliothèque de débogage.                                                                         |
| [**DisplayType**](displaytype.md)                     | Envoie des informations sur un type de média à l’emplacement de sortie de débogage.                                   |
| [**DumpGraph**](dumpgraph.md)                         | Envoie des informations sur un graphique de filtre à l’emplacement de sortie de débogage.                                 |
| [**GuidNames**](guidnames.md)                         | Tableau global qui contient des chaînes représentant les GUID définis dans UUID. h.                        |
| [**NOMME**](name.md)                                   | Génère une chaîne de débogage uniquement.                                                                       |
| [**OBSERVE**](note.md)                                   | Envoie une chaîne à l’emplacement de sortie de débogage.                                                         |
| [**AVERTI**](remind.md)                               | Génère un rappel au moment de la compilation.                                                                |



 

**Clés de Registre**

la fonction de sortie de débogage dans DirectShow utiliser un jeu de clés de registre. L’emplacement de ces clés de Registre dépend de la version de Windows.

*avant Windows Vista*, les clés de débogage se trouvent sous le chemin d’accès suivant :

**HKEY \_ \_** Débogage \\ **logiciel** \\  de l’ordinateur local

dans Windows Vista ou version ultérieure, ils se trouvent sous le chemin d’accès suivant :

**HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **DirectShow** \\ **Debug**

pour les filtres tiers, l’emplacement dépend de la version du [DirectShow Classes de Base](directshow-base-classes.md) qui a été utilisée pour générer le filtre. la version incluse dans le SDK Windows pour Windows Vista utilise le chemin d’accès le plus récent. Les versions précédentes utilisaient l’ancien chemin d’accès.

Dans les notes qui suivent, l’étiquette *&lt; DebugRoot &gt;* est utilisée pour indiquer ces deux chemins d’accès. remplacez le chemin d’accès correct, selon la version de Windows ou la version des classes de base.

**Journalisation du débogage**

DirectShow définit plusieurs types de messages, comme indiqué dans le tableau suivant.



| Valeur                   | Description                                             |
|-------------------------|---------------------------------------------------------|
| erreur de journal \_              | Notification d’erreur.                                     |
| verrouillage du journal \_            | Verrouillage et déverrouillage des sections critiques.             |
| mémoire de JOURNALisation \_             | Allocation de mémoire, et création et destruction d’objets. |
| synchronisation du journal \_             | Mesures de minutage et de performances.                    |
| suivi du journal \_              | Suivi des appels généraux.                                   |
| CUSTOM1 à CUSTOM5 | Disponible pour les messages de débogage personnalisés                     |



 

chaque fonction de journalisation de débogage DirectShow spécifie un type de message et un niveau de journal. Le message de débogage s’affiche uniquement lorsque le niveau de débogage actuel de ce type de message est supérieur ou égal au niveau spécifié dans la fonction de journalisation. Dans le cas contraire, le message est ignoré.

Par exemple, le code suivant génère la chaîne « This is a Debug message » si le niveau de trace du journal \_ est supérieur ou égal à 3 :

``` syntax
DbgLog((LOG_TRACE, 3, TEXT("This is a debug message")));
```

Chaque module peut définir son propre niveau de débogage pour chaque type de message. (Un *module* est une dll ou un fichier exécutable qui peut être chargé à l’aide de la fonction **LoadLibrary** .) Les niveaux de débogage d’un module s’affichent dans le Registre sous la clé suivante :

**HKEY \_ \_** \\ **&lt; DebugRoot &gt;** \\ **&lt; modulename &gt;** de l’ordinateur \\ **&lt; local &gt;**

où *<Message Type>* est le type de message moins le « journal \_ » initial, par exemple, le **verrouillage** des messages de verrouillage des journaux \_ . Quand un module est chargé, la bibliothèque de débogage recherche les niveaux de journalisation du module dans le registre. Si les clés de Registre n’existent pas, la bibliothèque de débogage les crée.

Un module peut également définir ses propres niveaux au moment de l’exécution, à l’aide de la fonction [**DbgSetModuleLevel**](dbgsetmodulelevel.md) . Pour envoyer un message à la sortie de débogage, appelez la macro [**DbgLog**](dbglog.md) . L’exemple suivant crée un message de niveau 3 de type \_ trace du journal :

Vous pouvez également spécifier des niveaux de journalisation globale, avec la clé de Registre suivante :


```C++
\HKEY_LOCAL_MACHINE\<DebugRoot>\GLOBAL\<Message Type>
```



La bibliothèque de débogage utilise le niveau le plus élevé, le niveau global ou le niveau du module.

**Emplacement de sortie de débogage**

L’emplacement de sortie de débogage est déterminé par une autre clé de Registre :

**HKEY \_ \_Ordinateur local** \\ **&lt; DebugRoot &gt;** \\ **<Modile Name>** \\ **LogToFile**

Si la valeur de cette clé est `Console` , la sortie est envoyée à la fenêtre de console. Si la valeur est `Deb` , `Debug` , `Debugger` ou une chaîne vide, la sortie est envoyée à la fenêtre du débogueur. Dans le cas contraire, la sortie est écrite dans un fichier spécifié par la clé de registre.

avant qu’un exécutable n’utilise la bibliothèque de débogage DirectShow, il doit appeler la fonction [**DbgInitialise**](dbginitialise.md) . Ensuite, il doit appeler la fonction [**DbgTerminate**](dbgterminate.md) . Les dll n’ont pas besoin d’appeler ces fonctions, car le point d’entrée de la DLL (défini dans la bibliothèque de classes de base) les appelle automatiquement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilitaires de débogage](debugging-utilities.md)
</dt> </dl>

 

 



