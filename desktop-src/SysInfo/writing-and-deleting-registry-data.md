---
description: Une application peut utiliser la fonction RegSetValueEx pour associer une valeur et ses données à une clé. Pour obtenir la liste des types de valeurs pris en charge par RegSetValueEx, consultez types de valeur de registre.
ms.assetid: 75ac826a-f169-400c-b6d6-3e3ec9ebf996
title: Écriture et suppression de données de Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5185c98f39a37512ec56fb994d5f1c4ba4b61ee
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368551"
---
# <a name="writing-and-deleting-registry-data"></a>Écriture et suppression de données de Registre

Une application peut utiliser la fonction [**RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa) pour associer une valeur et ses données à une clé. Pour obtenir la liste des types de valeurs pris en charge par **RegSetValueEx**, consultez [types de valeur de registre](registry-value-types.md).

Pour supprimer une valeur d’une clé, une application peut utiliser la fonction [**RegDeleteValue**](/windows/desktop/api/Winreg/nf-winreg-regdeletevaluea) . Pour supprimer une clé, elle peut utiliser la fonction [**RegDeleteKey**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeya) . Une clé supprimée n’est pas supprimée tant que le dernier descripteur n’a pas été fermé. Les sous-clés et les valeurs ne peuvent pas être créées sous une clé supprimée.

Il n’est pas possible de verrouiller une clé de Registre pendant une opération d’écriture pour synchroniser l’accès aux données. Toutefois, vous pouvez contrôler l’accès à une clé de Registre à l’aide des attributs de sécurité. Pour plus d’informations, consultez sécurité de la [clé de Registre et droits d’accès](registry-key-security-and-access-rights.md).

Plusieurs opérations de Registre peuvent être effectuées au sein d’une même transaction. Pour associer une clé de Registre à une transaction, une application peut utiliser la fonction [**RegCreateKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeytransacteda) ou [**RegOpenKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regopenkeytransacteda) . Pour plus d’informations sur les transactions, consultez [Gestionnaire de transactions du noyau](/windows/desktop/Ktm/kernel-transaction-manager-portal).

 

 
