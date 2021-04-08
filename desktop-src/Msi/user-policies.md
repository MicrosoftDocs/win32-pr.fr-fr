---
description: Stratégies de système utilisateur utilisées avec l’Windows Installer.
ms.assetid: 74e940a1-dc7c-4ea3-ab62-d118204dac3e
title: Stratégies utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26cec4066e4d8267b2750d538e691d91382550fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862034"
---
# <a name="user-policies"></a>Stratégies utilisateur

Les stratégies d’utilisateur suivantes peuvent être configurées sous

**HKEY \_ \_** \\ **Stratégies logicielles** de l’utilisateur actuel \\  \\ **Microsoft** \\ **Windows** \\ **installer**



| Nom de la valeur                                                            | Types de données de valeur          | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AlwaysInstallElevated a](alwaysinstallelevated.md)<br/>         | **\_valeur DWORD reg**<br/> | Si cette valeur est définie sur « 1 » et que la valeur de l’ordinateur correspondant est également définie, le programme d’installation installe toujours avec des privilèges élevés.<br/> Dans le cas contraire, le programme d’installation utilise des privilèges élevés pour installer les applications managées et utilise le niveau de privilège de l’utilisateur actuel pour les applications non gérées.<br/>                                                                                                                                                                                                      |
| [DisableMedia](disablemedia.md)<br/>                           | **\_valeur DWORD reg**<br/> | Si la stratégie [DisableMedia](disablemedia.md) est définie sur « 1 », les utilisateurs et les administrateurs qui exécutent une installation de maintenance d’un produit ne peuvent pas utiliser la boîte de dialogue Parcourir pour parcourir les sources de média, telles que les CD-ROM, pour les sources d’autres produits installables. La recherche d’autres produits est empêchée, que l’installation soit avec des privilèges élevés. Il est toujours possible pour l’utilisateur de réinstaller le produit à partir d’un support si celui-ci possède une source de média correctement libellée.<br/> |
| [DisableRollback](disablerollback.md)<br/>                     | **\_valeur DWORD reg**<br/> | Si cette valeur est définie sur « 1 », le programme d’installation ne stocke pas les fichiers de restauration lors de l’installation, ce qui désactive la restauration de l’installation. Par défaut, la restauration est activée. Les administrateurs sont invités à ne pas utiliser cette stratégie, sauf si elle est absolument essentielle.<br/>                                                                                                                                                                                                                                                             |
| [SearchOrder](searchorder.md)<br/>                             | **SZ de REG \_**<br/>    | Ordre dans lequel le programme d’installation recherche les trois différents types de sources :<br/> « n » – réseau<br/> « m » – média (CD-ROM ou DVD)<br/> "u" – URL (Uniform Resource Locator)<br/> Par exemple, la valeur « NMU » indique au programme d’installation de rechercher d’abord les sources réseau, les sources de média et les sources d’URL. Le fait de laisser une lettre supprime le type de volume correspondant de la recherche. L’ordre par défaut en l’absence de cette valeur est réseau en premier, puis média suivi par URL.<br/>          |
| [Stratégie TransformsAtSource](transformsatsource-policy.md)<br/> | **\_valeur DWORD reg**<br/> | Si cette valeur existe et est définie sur « 1 »; le programme d’installation recherche les fichiers de transformation à la racine de toutes les sources réseau [**dans la source d’alimentation**](sourcelist.md) du produit. Par défaut, les transformations sont stockées dans le dossier Application Data du profil d’un utilisateur.<br/>                                                                                                                                                                                                                                             |



 

 

 




