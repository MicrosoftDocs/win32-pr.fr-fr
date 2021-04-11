---
title: Ajout de la fonctionnalité Microsoft Agent à votre application
description: Ajout de la fonctionnalité Microsoft Agent à votre application
ms.assetid: 2b4816dd-11bf-4c17-873e-4bdbb7fa1ccf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a2972b0251a4114e5d280d8f739d416ebc5dc1c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314837"
---
# <a name="adding-microsoft-agent-functionality-to-your-application"></a>Ajout de la fonctionnalité Microsoft Agent à votre application

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Pour accéder aux interfaces serveur de Microsoft Agent, l’agent doit déjà être installé sur le système cible. L’installation autre que l’utilisation du fichier exécutable d’installation automatique de l’agent, telle que la tentative de copie et l’inscription des fichiers de composants de l’agent, n’est pas prise en charge. Cela garantit une installation cohérente et complète. Notez que le fichier d’installation automatique de Microsoft Agent ne s’installe pas sur les systèmes d’exploitation Microsoft Windows 2000 et versions ultérieures, car ces versions du système d’exploitation incluent déjà leur propre version de l’agent.

Pour installer correctement l’agent sur un système cible disposant d’un système d’exploitation Microsoft Windows antérieur, vous devez également vous assurer que le système cible dispose d’une version récente du Microsoft Visual C++ Runtime (Msvcrt.dll), de l’outil d’inscription Microsoft (Regsvr32.dll) et des dll Microsoft COM. Le moyen le plus simple de s’assurer que les composants nécessaires se trouvent sur le système cible est d’exiger l’installation de Microsoft Internet Explorer 3,02 ou version ultérieure. Vous pouvez également installer les deux premiers composants qui sont disponibles dans le cadre de Microsoft Visual C++. Les DLL COM nécessaires peuvent être installées dans le cadre de la mise à jour Microsoft DCOM, disponible sur le site Web de Microsoft. Vous trouverez des informations supplémentaires et des informations de licence pour ces composants sur le site Web de Microsoft.

Les composants de langue de l’agent peuvent être installés de la même façon. De même, vous pouvez utiliser cette technique pour installer le format des services ACS des caractères Microsoft disponibles pour la distribution à partir du site Web de Microsoft Agent. Les fichiers de caractères sont automatiquement installés dans le \\ sous-répertoire Microsoft Agent chars.

Étant donné que les composants de Microsoft Agent sont conçus en tant que composants du système d’exploitation, l’agent n’est peut-être pas désinstallé. De même, si l’agent est déjà installé en tant que partie du système d’exploitation Windows, le cabinet à installation automatique de l’agent peut ne pas s’installer.

Une fois installé, pour appeler les interfaces de l’agent, créez une instance du serveur et demandez un pointeur vers une interface spécifique que le serveur prend en charge à l’aide de la Convention COM standard. En particulier, la bibliothèque COM fournit une fonction API, [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance), qui crée une instance de l’objet et retourne un pointeur vers l’interface demandée de l’objet. Demandez un pointeur vers l’interface [**IAgent**](iagent.md) ou [**IAgentEx**](iagentex.md) dans votre appel **CoCreateInstance** ou dans un appel ultérieur à [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).

Le code suivant illustre cela en C/C++.


```
hRes = CoCreateInstance(CLSID_AgentServer,
                     NULL,
                     CLSCTX_SERVER,
                     IID_IAgentEx,
                     (LPVOID *)&amp;pAgentEx);
```



Si le serveur Microsoft Agent est en cours d’exécution, cette fonction se connecte au serveur. dans le cas contraire, il démarre le serveur.

Notez que les interfaces du serveur Microsoft Agent incluent souvent des interfaces étendues qui incluent un suffixe « ex ». Ces interfaces sont dérivées de et, par conséquent, incluent toutes les fonctionnalités de, leurs équivalents non-ex. Si vous souhaitez utiliser l’une des fonctionnalités étendues, utilisez les interfaces ex.

Les fonctions qui acceptent des pointeurs vers des BSTR allouent de la mémoire à l’aide de [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring). Il incombe à l’appelant de libérer cette mémoire à l’aide de [**SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring).

 

 