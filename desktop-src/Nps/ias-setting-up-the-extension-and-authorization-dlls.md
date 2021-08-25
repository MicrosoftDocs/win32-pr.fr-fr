---
title: Configuration des dll d’extension
description: Au démarrage, NPS vérifie dans le registre la liste des dll tierces à appeler.
ms.assetid: fbbd9031-3ebe-47b8-8d8b-e359fa7d4b67
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 737d53bd25a28321c333e890a019af881ae54fa1c5ae92299b1776689f9abb74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962509"
---
# <a name="setting-up-the-extension-dlls"></a>Configuration des dll d’extension

> [!Note]  
> le Service d’authentification Internet (IAS) a été renommé serveur nps (network Policy Server) à partir de Windows Server 2008. Le contenu de cette rubrique s’applique à IAS et à NPS. Dans le texte, NPS est utilisé pour faire référence à toutes les versions du service, y compris les versions initialement appelées IAS.

 

Au démarrage, NPS vérifie dans le registre la liste des dll tierces à appeler.

Pour configurer une DLL d’authentification ou d’autorisation sur un serveur NPS, répertoriez les chemins d’accès aux dll dans les valeurs sous la clé de Registre suivante :

**\\Paramètres de \\ AuthSrv des services de CurrentControlSet du système HKLM \\ \\ \\\\**

Si les clés **AuthSrv** et **Parameters** n’existent pas, créez-les.

La valeur d’énumération des dll d’extension d’authentification est la suivante :

**ExtensionDLLs**

La valeur dans laquelle répertorier les dll d’extension d’autorisation est :

**AuthorizationDLLs**

Les valeurs **ExtensionDLLs** et **AuthorizationDLLs** doivent être de type **reg \_ multi \_ SZ**. Ce type vous permet de répertorier plusieurs dll.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Appel des dll d’extension](/windows/desktop/Nps/ias-authentication-and-authorization-process)
</dt> <dt>

[Attributs d’identification utilisateur](/windows/desktop/Nps/ias-user-identification-attributes)
</dt> </dl>

 

 