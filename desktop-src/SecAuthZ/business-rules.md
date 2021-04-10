---
description: Une règle d’entreprise permet à une application d’utiliser la logique au moment de l’exécution pour qualifier les autorisations accordées au client.
ms.assetid: 2220d533-87f5-41a6-a688-a3307f0853fa
title: Règles d'entreprise
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f77d94ce623086b8850406f9bae4f412d3bbdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104211078"
---
# <a name="business-rules"></a>Règles d'entreprise

Une règle d’entreprise permet à une application d’utiliser la logique au moment de l’exécution pour qualifier les autorisations accordées au client.

Une règle d’entreprise est un script écrit dans le langage de programmation Visual Basic Scripting Edition (VBScript) ou écrit à l’aide du logiciel de développement Microsoft JScript qui est associé à un objet [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) . Lorsqu’une application vérifie l’accès pour une opération, le gestionnaire d’autorisations vérifie d’abord si le client actuel a accès à toutes les tâches qui contiennent cette opération, mais qui ne sont pas associées à des règles d’entreprise. Si l’accès n’est pas accordé de cette manière, le gestionnaire d’autorisations exécute des scripts de règle d’entreprise associés à toute tâche qui contient l’opération.

Une application transmet des informations à un script de règle d’entreprise sous la forme d’une paire de tableaux représentant les noms et les valeurs des paramètres. Le script a accès à ces paramètres par le biais d’un objet [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) qui est créé lors de l’exécution du script.

Un script de règle d’entreprise ne peut pas être assigné à une tâche contenue dans une étendue déléguée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Accès éligible avec la logique métier en C++](qualifying-access-with-business-logic-in-c--.md)
</dt> </dl>

 

 



