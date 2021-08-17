---
description: Les applications clientes qui appellent des interfaces WMI peuvent contrôler les niveaux de sécurité de leurs processus.
ms.assetid: 790b4e40-9b92-464a-a774-dec0b75cedee
ms.tgt_platform: multiple
title: Définition de la sécurité des processus d’application cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7be6b3f6e632ade53700bbe81afc7698a06fe2ff038e0c57c1b4a7eed44afa68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739468"
---
# <a name="setting-client-application-process-security"></a>Définition de la sécurité des processus d’application cliente

Les applications clientes qui appellent des interfaces WMI peuvent contrôler les niveaux de sécurité de leurs processus. Toutes les applications WMI accèdent à WMI via COM, et vous pouvez appeler la fonction COM [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) pour définir la sécurité de vos processus. Les applications qui effectuent des appels asynchrones à WMI et aux applications qui s’inscrivent en tant que consommateurs d’événements définissent les niveaux de sécurité de l’appel dans WMI.

Si vous n’effectuez pas d’appel explicite à [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), com l’appelle implicitement avec les valeurs du Registre. Toutefois, les valeurs de Registre peuvent avoir des paramètres inférieurs pour l’emprunt d’identité et l’authentification qui ne fournissent pas la sécurité requise pour WMI. Pour plus d’informations, consultez [définition du niveau de sécurité de processus par défaut à l’aide de C++](setting-the-default-process-security-level-using-c-.md).

L’accès asynchrone à WMI n’est pas recommandé. Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur. Cela pose des risques de sécurité pour vos scripts et vos applications. Pour éliminer les risques, utilisez une communication semi-synchrone ou synchrone, ou effectuez des vérifications d’accès appropriées dans votre application cliente. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

Les appels à n’importe quel proxy WMI ([**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject),[**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)ou [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)) utilisent un pointeur hors processus. Pour plus d’informations sur les valeurs par défaut et les recommandations, consultez [définition de la sécurité sur IWbemServices et d’autres proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).

La procédure suivante décrit les étapes que vous devez effectuer pour définir la sécurité de WMI sur votre processus d’application.

**Pour définir la sécurité de WMI sur votre processus d’application**

1.  déterminez les niveaux de sécurité requis pour les systèmes d’exploitation Windows sur lesquels votre application cliente s’exécute.
2.  Appelez la fonction COM [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) pour définir la sécurité par défaut du processus dans lequel l’application cliente s’exécute. Cela permet de déclarer le niveau de sécurité requis par d’autres applications pour accéder au processus dans lequel votre application s’exécute.
3.  Si vous avez besoin de modifier la sécurité sur un proxy individuel, par exemple sur un autre appel à [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), appelez [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).
4.  Si vous devez contrôler le matériel distant ou un objet système qui nécessite davantage de privilèges, utilisez la fonction [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) pour activer les privilèges nécessaires. Notez que vous ne pouvez pas activer un privilège que le processus n’a pas déjà affecté. Pour plus d’informations, consultez la page [vérification de l’accès aux objets privés](/windows/desktop/SecAuthZ/checking-access-to-private-objects).

Pour plus d’informations sur la définition du niveau de sécurité de processus par défaut, consultez [définition du niveau de sécurité de processus par défaut à l’aide de C++](setting-the-default-process-security-level-using-c-.md) et [définition du niveau de sécurité de processus par défaut à l’aide de VBScript](setting-the-default-process-security-level-using-vbscript.md).

 

 
