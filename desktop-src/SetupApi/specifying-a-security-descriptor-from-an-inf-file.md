---
description: Vous pouvez contrôler la capacité d’un processus à accéder aux objets sécurisables ou à effectuer des tâches d’administration système.
ms.assetid: a5d8eaaa-4585-44a3-ab92-2a323d9af80c
title: Spécification d’un descripteur de sécurité à partir d’un fichier INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a065a41db49385c7c95e683fd4aca4cfe7eb9cd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952996"
---
# <a name="specifying-a-security-descriptor-from-an-inf-file"></a>Spécification d’un descripteur de sécurité à partir d’un fichier INF

Vous pouvez contrôler la capacité d’un processus à accéder aux objets sécurisables ou à effectuer des tâches d’administration système. Un objet sécurisable est un objet qui peut avoir un descripteur de sécurité. Tous les objets nommés sont sécurisables. Certains objets sans nom, tels que les objets de processus et de thread, peuvent également avoir des descripteurs de sécurité. Pour plus d’informations sur le contrôle de l’accès aux objets sécurisables, consultez [Access Control](/windows/desktop/SecAuthZ/access-control).

Les [descripteurs de sécurité](/windows/desktop/SecAuthZ/security-descriptors) contiennent les informations de sécurité associées aux objets sécurisables. Pour la plupart des objets sécurisables, vous pouvez spécifier le descripteur de sécurité d’un objet dans l’appel de fonction qui crée l’objet. Par exemple, vous pouvez spécifier un descripteur de sécurité dans les fonctions [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) et [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .

Pour définir un descripteur de sécurité à partir d’un fichier INF, ajoutez une section sécurité créée par l’enregistreur INF immédiatement après la section qui installe le fichier, la clé de registre ou le composant. La section sécurité doit contenir une ligne avec le descripteur de sécurité de chaîne écrit en utilisant le format pour les [chaînes de descripteur de sécurité](/windows/desktop/SecAuthZ/security-descriptor-strings). La ligne doit également être placée entre guillemets (").

Par exemple, l’extrait de code fichier INF suivant crée une clé de Registre à laquelle seuls les administrateurs et le système ont accès. Notez que cet exemple requiert des privilèges d’administrateur.

``` syntax
[DDInstall]
AddReg=mydevice.reg
 
[mydevice.reg]
include Registry information here
 
[mydevice.reg.Security]
"D:P(A;CI;GA;;;BA)(A;CI;GA;;;SY)"
```

Dans ce cas, la signification de la chaîne est que les administrateurs disposent d’un contrôle total, que le système dispose d’un contrôle total et que l’accès peut être hérité à toutes les sous-clés. Pour plus d’informations, consultez [langage de définition du descripteur de sécurité](/windows/desktop/SecAuthZ/security-descriptor-definition-language).

 

 
