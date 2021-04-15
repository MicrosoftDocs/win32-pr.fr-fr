---
description: Les périphériques SNMP sont accessibles en lisant ou en écrivant dans l’instance de classe correspondante dans le stockage SMIR WMI (référentiel des informations du module SNMP).
ms.assetid: af5e1321-b552-447e-a217-eecbebe1f203
ms.tgt_platform: multiple
title: Lecture et écriture dans des périphériques SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8fc25f384d499e16e19c5e909f7d091ea34f9a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528605"
---
# <a name="reading-from-and-writing-to-snmp-devices"></a>Lecture et écriture dans des périphériques SNMP

Les périphériques SNMP sont accessibles en lisant ou en écrivant dans l’instance de classe correspondante dans le stockage SMIR WMI (référentiel des informations du module SNMP). Lorsque vous travaillez avec plusieurs appareils du même type, pour des performances optimales, chargez l’MiB pour un type d’appareil SNMP dans le stockage SMIR.

> [!Note]  
> Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

Sélectionnez l’une des options suivantes pour lire ou écrire à partir de chaque type d’appareil SNMP en mettant à jour les informations de contexte de l’instance avant de communiquer avec chacune d’elles.

-   Utilisez un nom DNS au lieu de l’adresse IP lors du référencement d’un appareil spécifique.

    L’exemple suivant montre comment utiliser le nom DNS pour un appareil spécifique.

    ```VB
    strNamedValue = Context.Add("AgentAddress", "Router1" )
    ```

    

-   Créez un espace de noms distinct et associez une adresse d’appareil à l’objet d’espace de noms à l’aide du qualificateur d’instance AgentAddress afin que l’espace de noms soit définitivement lié à l’appareil. Dans ce cas, vous n’avez pas besoin de spécifier les informations de l’objet de contexte.
-   Lire à partir d’un périphérique SNMP.

    L’exemple suivant effectue une opération d’extraction sur une classe d’appareil.

    ```VB
    Set objLocator = CreateObject("wbemscripting.swbemlocator")
    Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")
    objServices.security_.privileges.AddAsString("SeSecurityPrivilege")
    Set objSet = objServices.ExecQuery _
        ("SELECT * FROM SNMP_NET_DEVICE_123 WHERE hdwr_idx>1",, _
          wbemFlagReturnWhenComplete)
    for each obj in objset 
      'do whatever 
    next
    ```

    

-   Écrire sur un périphérique SNMP.

    L’exemple suivant effectue une opération set sur une classe d’appareil.

    ```VB
    Set objLocator = CreateObject("wbemscripting.swbemlocator")
    Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")
    objServices.security_.privileges.AddAsString("SeSecurityPrivilege")
    Set obj= objServices.Get("SNMP_NET_DEVICE_123=@")
    obj.deviceLocation = "40/5073"
    obj.put_
    ```

    

Les classes corrélées sont celles qu’un appareil SNMP donné peut prendre en charge lorsque l’énumération se produit. La corrélation affecte l’ensemble des classes retournées à partir du stockage SMIR. L’énumération non corrélée retourne toutes les classes présentes dans le stockage SMIR, que l’appareil les prenne en charge ou non. Pour plus d’informations sur l’utilisation des techniques de corrélation WMI, consultez [corrélation de classe SNMP WMI](wmi-snmp-class-correlation.md).

 

 



