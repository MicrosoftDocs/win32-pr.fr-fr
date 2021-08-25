---
title: Boîtes de dialogue courantes RAS
description: Windows fournit un ensemble de fonctions qui affichent les boîtes de dialogue RAS fournies par le système.
ms.assetid: 8231511a-7339-4fbb-8a39-f643ac575856
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be93db8e8d1819abe56d98bb293a7b6b027089be0648b00f7848d5204e911ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909719"
---
# <a name="ras-common-dialog-boxes"></a>Boîtes de dialogue courantes RAS

Windows fournit un ensemble de fonctions qui affichent les boîtes de dialogue RAS fournies par le système. Ces fonctions permettent aux applications d’afficher facilement une interface utilisateur familière afin que les utilisateurs puissent effectuer des tâches RAS. Par exemple, les utilisateurs peuvent établir et surveiller des connexions ou utiliser des entrées d’annuaire téléphonique. Windows 95 ne prend pas en charge ces fonctions pour le moment.

La fonction [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) affiche la boîte de dialogue principale d' **accès réseau à distance** . À partir de cette boîte de dialogue, l’utilisateur peut composer, modifier ou supprimer une entrée de l’annuaire téléphonique sélectionnée, créer une nouvelle entrée de l’annuaire téléphonique ou spécifier les préférences de l’utilisateur. La fonction **RasPhonebookDlg** utilise la structure [**RASPBDLG**](/previous-versions/windows/desktop/legacy/aa377607(v=vs.85)) pour spécifier des paramètres d’entrée et de sortie supplémentaires. Par exemple, vous pouvez définir des membres de la structure pour contrôler la position de la boîte de dialogue à l’écran. Vous pouvez utiliser la structure **RASPBDLG** pour spécifier une fonction de rappel [**RasPBDlgFunc**](/windows/desktop/api/Rasdlg/nc-rasdlg-raspbdlgfunca) qui reçoit les notifications de l’activité de l’utilisateur pendant que la boîte de dialogue est ouverte. Par exemple, RAS appelle votre fonction **RasPBDlgFunc** si l’utilisateur compose, modifie, crée ou supprime une entrée d’annuaire téléphonique.

Vous pouvez utiliser la fonction [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) pour démarrer une opération de connexion RAS sans afficher la boîte de dialogue principale d' **accès réseau à distance** . Avec **RasDialDlg**, vous spécifiez un numéro de téléphone ou une entrée d’annuaire téléphonique à appeler. La fonction affiche un flux de boîtes de dialogue qui indiquent l’état de l’opération de connexion. La fonction **RasDialDlg** utilise une structure [**RasDialDlg**](/previous-versions/windows/desktop/legacy/aa377023(v=vs.85)) pour spécifier des paramètres d’entrée et de sortie supplémentaires, tels que la position de la boîte de dialogue et la sous-entrée de l’annuaire téléphonique à appeler.

Pour afficher la feuille de propriétés d' **accès réseau à distance** , appelez la fonction [**RasMonitorDlg**](/previous-versions/windows/desktop/legacy/aa377584(v=vs.85)) . Cette boîte de dialogue permet à l’utilisateur de surveiller l’état des connexions existantes. La fonction **RasMonitorDlg** utilise une structure [**RasMonitorDlg**](/previous-versions/windows/desktop/legacy/aa377591(v=vs.85)) pour spécifier des paramètres d’entrée et de sortie supplémentaires, tels que la position de la boîte de dialogue et la page de la feuille de propriétés à afficher en haut.

Vous pouvez appeler la fonction [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) pour afficher une feuille de propriétés permettant de créer, de modifier ou de copier une entrée d’annuaire téléphonique. La fonction **RasEntryDlg** utilise une structure [**RasEntryDlg**](/previous-versions/windows/desktop/legacy/aa377260(v=vs.85)) pour spécifier des paramètres d’entrée et de sortie supplémentaires, tels que la position de la boîte de dialogue et le type d’opération de l’annuaire téléphonique.

 

 