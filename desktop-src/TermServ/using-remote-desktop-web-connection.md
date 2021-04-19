---
title: Utilisation du contrôle ActiveX Bureau à distance
description: Comment vous pouvez utiliser le contrôle ActiveX Bureau à distance pour personnaliser l’expérience utilisateur Services Bureau à distance.
ms.assetid: ea80a99a-7bf6-48e2-8bd0-c9a158bcf475
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance Services Bureau à distance à l’aide du contrôle ActiveX Bureau à distance
- Services Bureau à distance Connexion Bureau à distance par le Web, utilisation
- protocole RDP (Remote Desktop Protocol) Services Bureau à distance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b06f575d5cffc16bd19f6bbe5fd4b3237dda7b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511006"
---
# <a name="using-the-remote-desktop-activex-control"></a>Utilisation du contrôle ActiveX Bureau à distance

Les rubriques suivantes contiennent des informations sur la façon dont vous pouvez utiliser le contrôle ActiveX Bureau à distance pour personnaliser l’expérience utilisateur Services Bureau à distance.

Le contrôle ActiveX Bureau à distance est disponible sous les formes suivantes :

-   **Le contrôle scriptable**: implémente des interfaces sécurisées pour l’écriture de scripts. Cette forme du contrôle peut être utilisée par les clients Web ou les hôtes de script (tels que VBScript).
-   **Le contrôle non scriptable**, offre des fonctionnalités supplémentaires qui ne sont pas sûres pour les scripts. Cette forme du contrôle peut être utilisée à partir du code natif ou managé, mais ce formulaire ne peut pas être utilisé par les clients Web ou les hôtes de script uniquement.

La liste suivante contient les **CLSID** des différents contrôles pour les différentes versions de système d’exploitation. Chacun des **CLSID** s est compatible avec les versions ultérieures du système. Par exemple, le **CLSID** du contrôle scriptable sur Windows Vista fonctionnera sur les versions ultérieures du système, telles que Windows 7.



| Version du système                          | CLSID du contrôle scriptable             | CLSID de contrôle ne pouvant pas être scriptable          |
|-----------------------------------------|--------------------------------------|--------------------------------------|
| Windows 8.1, Windows Server 2012 R2     | 301B94BA-5D25-4A12-BFFE-3B6E7A616585 | 8B918B82-7985-4C24-89DF-C33AD2BBFBCD |
| Windows 8, Windows Server 2012          | 5F681803-2900-4C43-A1CC-CF405404A676 | A3BC03A0-041D-42E3-AD22-882B7865C9C5 |
| Windows 7, Windows Server 2008          | A9D7038D-B5ED-472E-9C47-94BEA90A5910 | 54D38BF7-B1EF-4479-9674-1BD6EA465258 |
| Windows Vista Service Pack 1 (SP1) | 7390F3D8-0439-4C05-91E3-CF5CB290C3D0 | D2EA46A7-C2BF-426B-AF24-E19C44456399 |
| Windows Vista                           | 4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2 | 4EB2F086-C818-447E-B32C-C51CE2B30D31 |



 

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[Incorporation du contrôle Bureau à distance ActiveX dans une page Web](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
</dt> <dd>

Exemple illustrant l’utilisation des interfaces scriptables.

</dd> <dt>

[Implémentation de canaux virtuels scriptables à l’aide de Connexion Bureau à distance par le Web](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md)
</dt> <dd>

Exemples de code qui illustrent les étapes d’implémentation de canaux virtuels scriptables avec Connexion Bureau à distance par le Web.

</dd> <dt>

[Utilisation du contrôle ActiveX Bureau à distance avec des canaux virtuels](using-the-remote-desktop-activex-control-with-virtual-channels.md)
</dt> <dd>

Si vous avez activé une application de canaux virtuels dans votre déploiement Services Bureau à distance, vous pouvez mettre cette application à la disposition des ordinateurs clients.

</dd> <dt>

[Exemple de page Web inclus avec le contrôle ActiveX Bureau à distance](sample-web-page-included-with-the-remote-desktop-activex-control.md)
</dt> <dd>

Un exemple de page Web (Default.htm) se trouve dans le répertoire d’installation de Connexion Bureau à distance par le Web.

</dd> <dt>

[Fournir la sécurité du client RDP](providing-for-rdp-client-security.md)
</dt> <dd>

Certaines propriétés de l’objet de contrôle ActiveX Bureau à distance sont limitées à des zones de sécurité d’URL Internet Explorer spécifiques.

</dd> <dt>

[Désactivation des fonctionnalités de Services Bureau à distance](disabling-terminal-services-features.md)
</dt> <dd>

Pour renforcer la sécurité, vous pouvez choisir de désactiver les fonctionnalités de Services Bureau à distance.

</dd> </dl>

Pour plus d’informations sur l’exemple de page Web inclus avec l’installation du contrôle ActiveX Bureau à distance, consultez [exemple de page Web inclus avec le contrôle activex Bureau à distance](sample-web-page-included-with-the-remote-desktop-activex-control.md).

 

 




