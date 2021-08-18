---
description: Après avoir développé un fournisseur de support de sécurité/une bibliothèque de liens dynamiques (DLL) de package d’authentification contenant un ou plusieurs packages de sécurité personnalisés, vous devez l’inscrire.
ms.assetid: db0d899e-dbd4-40d3-98d8-4d9668c01453
title: Inscription des dll SSP/AP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6405dc5ddce32ad5e4d87ed44f9344240b491fdc0ea789c30d5475ac6e73aaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919499"
---
# <a name="registering-sspap-dlls"></a>Inscription des dll SSP/AP

Après avoir développé [](../secgloss/s-gly.md)une / bibliothèque de liens dynamiques (dll) de [*package d’authentification*](../secgloss/a-gly.md) du fournisseur de support de sécurité (SSP/AP) contenant un ou plusieurs [*packages de sécurité*](../secgloss/s-gly.md)personnalisés, vous devez l’inscrire. Pour ce faire, ajoutez le nom de votre DLL SSP/AP personnalisée aux données de la valeur de Registre suivante :

**HKEY \_ \_** Packages de \\  \\  \\  \\  \\ **sécurité** LSA de contrôle de système d’ordinateur local

Les données de cette valeur de Registre sont une liste des noms des dll SSP/AP, sans l’extension « .dll ». Le type de données de cette liste **est \_ reg \_ multisz** , ce qui signifie qu’il doit y avoir un caractère null (« \\ 0 ») entre chaque nom de dll dans la liste.

En règle générale, les dll SSP/AP sont stockées dans le répertoire% SystemRoot%/system32 S’il s’agit du chemin d’accès à votre DLL SSP/AP personnalisée, n’incluez pas le chemin d’accès en tant que partie du nom de la DLL. Toutefois, si la DLL se trouve dans un chemin d’accès différent, incluez le chemin d’accès complet à la DLL dans le nom.

Chaque fois que le système démarre, le LSA charge les dll SSP/AP dans cette liste et exécute la séquence d’initialisation décrite dans l' [initialisation du mode LSA](lsa-mode-initialization.md).

### <a name="registering-a-custom-security-package-as-the-default-tls-ssp"></a>Inscription d’un package de sécurité personnalisé en tant que SSP TLS par défaut

Après avoir développé un fournisseur de support de sécurité TLS personnalisé et l’avoir inscrit comme décrit ci-dessus, vous devez également l’inscrire en tant que « SSP TLS par défaut ». Pour ce faire, renseignez le nom du package de votre SSP personnalisé sur les données de la valeur de Registre suivante :

**HKEY \_ Système d' \_ ordinateur local** \\ **système** de \\ **CurrentControlSet** \\ **contrôle** de l' \\ **autorité de certification** \\ **SSP TLS par défaut**

Les données de cette valeur de Registre sont le nom du package SSP, et non le nom de la dll. Le type de données est **reg \_ SZ**.

Les applications en mode utilisateur qui utilisent « TLS TLS par défaut » utilisent la valeur par défaut inscrite ici. Les applications en mode noyau ou les applications en mode utilisateur qui utilisent le « fournisseur de protocole de sécurité unifié Microsoft » ou d’autres noms de SSP TLS spécifiques ne seront pas affectés par cette modification.

> [!Note]  
> Ces informations de Registre se rapportent uniquement aux DLL SSP/AP. Pour plus d’informations sur l’inscription des fournisseurs de support de sécurité (SSP), consultez [écriture et installation d’un fournisseur de support de sécurité](writing-and-installing-a-security-support-provider.md). Pour plus d’informations sur les différences entre les dll SSP/AP et SSP, consultez [SSP/APS](ssp-aps-versus-ssps.md)et ssp.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Restrictions concernant l’inscription et l’installation d’un package de sécurité](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
