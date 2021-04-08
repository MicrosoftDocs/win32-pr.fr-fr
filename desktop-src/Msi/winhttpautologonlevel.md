---
description: La stratégie de connexion automatique (ouverture de session automatique) détermine le moment où il est acceptable pour WinHTTP d’inclure les informations d’identification par défaut dans une demande au serveur.
ms.assetid: 4ED8B6BC-E52D-4DE9-A9AE-1FDF61A978A9
title: WinHttpAutoLogonLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7760faa94e24b7fe5b33717c504b03e4de42c0aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866053"
---
# <a name="winhttpautologonlevel"></a>WinHttpAutoLogonLevel

La stratégie de connexion automatique (ouverture de session automatique) détermine le moment où il est acceptable pour *WinHTTP* d’inclure les informations d’identification par défaut dans une demande au serveur.

Vous pouvez définir cette valeur sur **L** pour le niveau de sécurité le plus bas du niveau de **\_ \_ sécurité \_ \_ WinHTTP**, définir sur **M** **pour \_ \_ \_ \_ le** niveau de sécurité de l'  ouverture de la configuration de l' **\_ ouverture \_ \_ \_** de Le niveau par défaut est **WinHTTP \_ Autologon \_ niveau de sécurité \_ \_ moyen**. Pour plus d’informations sur la stratégie de connexion automatique, consultez la section relative à [l’authentification dans WinHTTP](../winhttp/authentication-in-winhttp.md).

**Windows 8 et Windows Server 2012 :** Cette stratégie requiert Windows Installer s’exécutant sur Windows 8 ou Windows Server 2012 et n’est pas disponible sur toutes les versions antérieures de Windows.

## <a name="registry-key"></a>Clé de Registre

**HKEY \_ \_** \\ **Stratégies logicielles** de l’ordinateur local \\  \\ **Microsoft** \\ **Windows** \\ **installer**

## <a name="data-type"></a>Type de données

**SZ de REG \_**

 

 
