---
title: Installation d’EAP
description: Les fournisseurs implémentent EAPs, également appelés protocoles d’authentification, dans les bibliothèques de liens dynamiques (dll).
ms.assetid: af10b1e9-45c9-4640-ba79-fc9c23cc3c47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 619505a55108ebde0e14d7ff20c78394c6c90fad
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104381269"
---
# <a name="eap-installation"></a>Installation d’EAP

Les fournisseurs implémentent EAPs, également appelés protocoles d’authentification, dans les bibliothèques de liens dynamiques (dll). Une DLL pour le protocole d’authentification doit résider sur les ordinateurs client et serveur. Par souci de simplicité, les dll du client et du serveur peuvent être identiques. Toutefois, cela n’est pas obligatoire. Sachez également que la même DLL peut prendre en charge plusieurs protocoles d’authentification.

Le fournisseur doit fournir un logiciel d’installation pour installer et supprimer la DLL. Le logiciel d’installation doit également créer les clés et valeurs appropriées pour le protocole d’authentification dans le registre système, puis les supprimer lors de la désinstallation.

L’installation de chaque DLL EAP doit créer la clé de Registre suivante.

**HKEY \_ LOCAL \_ machine** \\ **System système** \\ **CurrentControlSet** \\ **services** \\ **rasman** \\ **PPP** \\ **EAP** \\ **&lt; eaptypeid &gt;**

Dans le chemin d’accès précédent, **&lt; eaptypeid &gt;** est l’ID du protocole d’authentification. Le fournisseur doit obtenir cet ID auprès de l’IANA (Internet Assigned Numbers Authority).

Pour plus d’informations et pour obtenir une description des valeurs prises en charge pour cette clé, consultez [valeurs de Registre du protocole d’authentification](authentication-protocol-registry-values.md).

 

 




