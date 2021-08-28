---
title: Classes et serveurs
description: Classes et serveurs
ms.assetid: cc88be56-0d96-47d2-b23b-6a6ad376bdae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30b87ce6b52e73f8ac4e465202b787a2c65dc563f3d7c0678ef82b91601351d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993799"
---
# <a name="classes-and-servers"></a>Classes et serveurs

COM utilise **la \_ \_ racine de classes HKEY** pour les paramètres au niveau de l’ordinateur, mais permet également une configuration par utilisateur des CLSID pour une sécurité et une flexibilité accrues. COM First consulte les classes de logiciels de l' **\_ \_ utilisateur \\ \\ actuel HKEY** avant d’examiner la **\_ \_ racine des classes HKEY**. COM conserve les informations sur l’ordinateur relatives aux CLSID sous **le \_ \_ \\ CLSID racine** de la classe HKEY et conserve les informations de classe par utilisateur sous **HKEY \_ Current \_ User \\ Software \\ classes \\ CLSID**.

Les serveurs COM prennent en charge l’inscription automatique. Pour un serveur in-process, cela signifie que la DLL doit exporter les fonctions suivantes :

-   [**Accompli**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)
-   [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)

Vous devez exporter explicitement ces fonctions à l’aide d’un fichier de définition de module, de commutateurs de l’éditeur de liens ou de directives de compilateur. Le magasin de classes utilise ces fonctions pour configurer le registre local après le téléchargement du fichier sur l’ordinateur client. En plus de la Banque de classes, ces fonctions sont également utilisées par d’autres environnements pour installer des serveurs sur des ordinateurs hôtes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscription des applications COM](registering-com-applications.md)
</dt> </dl>

 

 