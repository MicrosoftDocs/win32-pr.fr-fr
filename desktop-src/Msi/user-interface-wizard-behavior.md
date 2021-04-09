---
description: Pour créer une interface utilisateur simple, les développeurs de packages d’installation peuvent utiliser une conception d’interface utilisateur qui respecte le comportement de l’Assistant Interface.
ms.assetid: c69ba452-3c2e-47d7-8ea0-8f8f9e6b58c8
title: Comportement de l’Assistant interface utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 045aa59fe510ff10f428d0a7c74549ce4d817157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760138"
---
# <a name="user-interface-wizard-behavior"></a>Comportement de l’Assistant interface utilisateur

Pour créer une interface utilisateur simple, les développeurs de packages d’installation peuvent utiliser une conception d’interface utilisateur qui respecte le comportement de l’Assistant Interface.

Le terme comportement de l’Assistant de l’interface utilisateur signifie que chaque boîte de dialogue d’une séquence contient un bouton de **>>suivant** , sur lequel l’utilisateur clique pour passer à la boîte de dialogue suivante après avoir entré des données ou configuré des informations dans la boîte de dialogue active. Si l’utilisateur décide de revenir en arrière et de modifier les informations entrées dans une boîte de dialogue précédente, chaque boîte de dialogue contient un bouton **<<précédent** sur lequel l’utilisateur clique pour revenir en arrière. À la fin de la séquence de l’Assistant, l’utilisateur clique sur un bouton **Terminer** pour commencer le processus d’installation.

L’interface utilisateur décrite dans l’exemple d’interface utilisateur adhère au comportement de l’Assistant interface utilisateur. Consultez [un exemple d’installation](an-installation-example.md).

 

 



