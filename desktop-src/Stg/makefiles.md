---
title: Makefiles
description: Les makefiles pour chacun des exemples de code de cette série sont des makefiles génériques Microsoft Win32 et sont destinés à être créés à partir de la fenêtre d’invite de commandes.
ms.assetid: f9944069-b536-4ae2-8411-f02c3a78978c
keywords:
- fichiers make structurés Stockage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a15fef5818c28986232e8c2a648f43bdc096832f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008916"
---
# <a name="makefiles"></a>Makefiles

Les makefiles pour chacun des exemples de code de cette série sont des makefiles génériques Microsoft Win32 et sont destinés à être créés à partir de la fenêtre d’invite de commandes. Ils partent du principe que les outils de compilation et de l’éditeur de liens de Microsoft requièrent une modification pour fonctionner avec d’autres outils. La plupart des commutateurs de ligne de commande du compilateur/de l’éditeur de liens sont spécifiés par les macros définies dans le fichier Makefile Win32. mak inclus dans le kit de développement logiciel (SDK) de la plateforme.

Le fichier Makeall.bat et chaque exemple de fichier Make de code respectif, prennent en charge les options communes, énumérées dans le tableau suivant, pour l’appel à partir de la fenêtre d’invite de commandes pour contrôler la nature de la Build.



| Appel NMAKE        | Appel de makeall          | Résultat                       |
|-------------------------|-----------------------------|------------------------------|
| **NMAKE**               | **makeall**                 | Compiler avec les informations de débogage.     |
| **NMAKE** **nodebug = 1** | **makeall** **« nodebug = 1 »** | Compilez sans informations de débogage.  |
| Profil **NMAKE** **= 1** | **makeall** **« Profile = 1 »** | Compiler avec les informations de profilage. |
| réglage **NMAKE** **= 1**    | **makeall** **« réglage = 1 »**    | Avec informations sur le tuner de la plage de travail. |
| **NMAKE** **Unicode = 1** | **makeall** **« Unicode = 1 »** | Compiler pour Unicode.         |
|  **nettoyage** NMAKE     | **makeall** **nettoyer**       | Supprimez les fichiers binaires temporaires.   |
| **NMAKE** **cleanall**  | **makeall** **cleanall**    | Supprimer tous les fichiers générés.  |



 

Pour les appels Makeall.bat, vous devez disposer des guillemets comme indiqué. Les options **nodebug**, **Profile** et **tune** s’excluent mutuellement : vous ne pouvez utiliser qu’une seule d’entre elles, ou None, pour une compilation/un lien donné. Pour compiler les exemples à exécuter avec des chaînes Unicode, utilisez l’option **« Unicode = 1 »** . la valeur par défaut consiste à compiler pour la prise en charge de chaînes ANSI traditionnelles, car vous pouvez ensuite exécuter sur n’importe quel système d’exploitation 32 bits Windows. vous pouvez effectuer librement la compilation et l’exécution avec ou sans Unicode sur Windows Server 2003 et versions ultérieures, et Windows 2000 et versions ultérieures. Sachez que APPUTIL est toujours compilé avec les mêmes options que les autres exemples de code que vous pouvez compiler séparément. Cela est particulièrement vrai pour l’option **« Unicode = 1 »** .

Vous pouvez utiliser un environnement de développement intégré (IDE) C++ 32 bits installé pour générer les exemples à l’aide des makefiles génériques fournis. Pour ce faire, vous devez dans votre IDE gérer les Makefiles génériques en tant que makefiles « externes ». Les makefiles fournis nécessitent un utilitaire make compatible avec Microsoft NMAKE.

La plupart des IDE C++ peuvent reconnaître ces makefiles comme externes et tout de même fournir de nombreux avantages de l’IDE en matière de modification et de génération. par exemple, dans Microsoft Visual Studio 97 ou version ultérieure, vous pouvez utiliser le menu fichier ouvrir l’espace de travail pour créer un espace de travail en ouvrant une copie correctement nommée (par exemple, Exeskel. mak) de l’exemple de fichier make Win32.

 

 




