---
description: Cette section fournit la liste des codes de retour WMI, des constantes symboliques, des valeurs littérales et des descriptions. Ces codes peuvent être renvoyés par des scripts, des applications C++ ou des commandes WMIC.
ms.assetid: 7ae47482-edf4-4aa4-858a-76e55f3cb0a3
ms.tgt_platform: multiple
title: Codes de retour WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e05455b109bd05b7a1693b8a05b13f6f7aeb646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521485"
---
# <a name="wmi-return-codes"></a>Codes de retour WMI

Cette section fournit la liste des codes de retour WMI, des constantes symboliques, des valeurs littérales et des descriptions. Ces codes peuvent être renvoyés par des scripts, des applications C++ ou des commandes [**WMIC**](wmic.md) .

Si une erreur se produit, WMI retourne l’un des codes d’erreur suivants sous la forme d’une valeur 32 bits où les deux bits de poids fort indiquent le code de gravité du message.

<dl> <dt>

<span id="0"></span>0
</dt> <dd>

Succès

</dd> <dt>

<span id="1"></span>1
</dt> <dd>

Informationnel

</dd> <dt>

<span id="2"></span>2
</dt> <dd>

Avertissement

</dd> <dt>

<span id="3"></span>1,3
</dt> <dd>

Error

</dd> </dl>

> [!Note]
>
> Si WMI renvoie des messages d’erreur, sachez qu’ils ne peuvent pas indiquer des problèmes dans le service WMI ou les fournisseurs WMI. Les échecs peuvent provenir d’autres parties du système d’exploitation et émerger comme des erreurs via WMI. Dans tous les cas, ne supprimez pas le référentiel WMI en tant que première action, car la suppression du dépôt peut endommager le système ou les applications installées.
>
> Pour obtenir plus d’informations sur la source du problème, vous pouvez télécharger et exécuter l’outil en ligne de commande [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) diagnostic. Cet outil génère un rapport qui peut généralement isoler la source du problème et fournir des instructions sur la façon de le résoudre. Le rapport aide également les services de support technique Microsoft à vous aider. Vous pouvez télécharger les WMI Diagnosis Utility [ici](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).

 

-   [**Constantes d’erreur WMI**](wmi-error-constants.md)
-   [**Constantes non-erreur WMI**](wmi-non-error-constants.md)

 

 



