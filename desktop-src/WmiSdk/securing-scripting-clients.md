---
description: Les scripts et les applications de Visual Basic doivent définir la sécurité DCOM, en particulier pour l’accès à distance, et peuvent également avoir besoin d’activer des privilèges.
ms.assetid: 4816914d-a1cf-47d8-af20-2b22c53042d6
ms.tgt_platform: multiple
title: Sécurisation des clients de script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c58a3dbade78b1dd81b0bf89eb867d8cd5c2f265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202166"
---
# <a name="securing-scripting-clients"></a>Sécurisation des clients de script

Les scripts et les applications de Visual Basic doivent définir la sécurité DCOM, en particulier pour l’accès à distance, et peuvent également avoir besoin d’activer des privilèges.

## <a name="default-access-permissions"></a>Autorisations d’accès par défaut

L’accès WMI diffère entre les ordinateurs locaux et distants. Pour plus d’informations, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).

Voici les autorisations d’accès par défaut par compte :

-   Tout le monde, LocalService, NetworkService

    Autorisation de lire ou d’écrire des données et d’exécuter des [*méthodes de fournisseur*](gloss-p.md) sur l’ordinateur local. Ces comptes ne peuvent pas créer de nouvelles classes ou installer de nouveaux fournisseurs.

-   Comptes d'administrateur

    Contrôle total sur l’ordinateur local. Lors de la connexion à un ordinateur distant, le compte doit également être un administrateur local sur l’ordinateur distant.

## <a name="securing-a-scripting-client"></a>Sécurisation d’un client de script

Les applications de script et de Visual Basic WMI doivent définir les niveaux de sécurité DCOM de manière appropriée pour les systèmes d’exploitation ciblés. Pour plus d’informations, consultez [définition du niveau de sécurité de processus par défaut à l’aide de VBScript](setting-the-default-process-security-level-using-vbscript.md).

Lorsque vous vous connectez à un ordinateur distant, vous devrez peut-être modifier le service (NTLM ou Kerberos) qui gère l’authentification. Pour plus d’informations, consultez [définition du service d’authentification à l’aide de VBScript](setting-the-authentication-service-using-vbscript.md).

L’accès à certaines classes ou données WMI peut nécessiter un privilège qui n’est pas activé. Par exemple, vous devez inclure le privilège de sécurité lors de la connexion à la classe [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)) . Pour plus d’informations, consultez [exécution d’opérations privilégiées à l’aide de VBScript](executing-privileged-operations-using-vbscript.md).

Si vous accédez à WMI à partir d’une page de Active Server (ASP), une configuration IIS est nécessaire. Pour plus d’informations, consultez [configuration d’IIS 5,0 et versions ultérieures pour les scripts ASP WMI](configuring-iis-5-for-wmi-asp-scripting.md).

Vous essayez peut-être de vous connecter à un espace de noms qui nécessite une connexion chiffrée, en d’autres termes, qui requiert un niveau d’authentification de pktPrivacy. Pour plus d’informations, consultez [définition du niveau de sécurité de processus par défaut à l’aide de VBScript](setting-the-default-process-security-level-using-vbscript.md).

 

 
