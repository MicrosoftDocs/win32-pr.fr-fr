---
title: Provisionner un profil Wi-Fi via un site web
description: Autorisez les utilisateurs à télécharger un profil à partir d’un site Web et à le configurer.
ms.topic: article
ms.date: 01/22/2020
ms.openlocfilehash: e34c83fbee100316256293e27eac96dae685c37d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517809"
---
# <a name="provision-a-wi-fi-profile-via-a-website"></a>Provisionner un profil Wi-Fi via un site web

le flux de travail décrit dans cette rubrique a été introduit dans Windows 10, version 2004. Cette rubrique montre comment configurer un site Web pour qu’un utilisateur puisse configurer un profil pour un réseau Passpoint (ou pour un réseau normal) avant de se déplacer dans la plage des points d’accès Wi-Fi correspondants. Un exemple de scénario est celui d’un utilisateur qui envisage de visiter un aéroport ou une conférence pour la première fois, et il souhaite préparer à l’avance en téléchargeant et en configurant un profil à la résidence.

En tant que développeur, vous activez le workflow en fournissant un profil XML et en configurant un site Web. Vos utilisateurs peuvent ensuite approvisionner un profil de Wi-Fi en le téléchargeant à partir de votre site Web via un navigateur Web. sur l’appareil de l’utilisateur, le profil de Wi-Fi est ensuite configuré à l’aide de l’activation d’URI et de l’application Windows **Paramètres** .

Ce flux de travail remplace le mécanisme dans Internet Explorer pour l’approvisionnement des profils Wi-Fi, qui s’appuie sur des API JavaScript spécifiques à Microsoft. Ce nouveau flux de travail est censé fonctionner avec tous les principaux navigateurs.

## <a name="the-workflow-in-more-detail"></a>Le flux de travail plus en détail

Vous pouvez activer ce flux de travail à partir d’un lien hypertexte qui comprend comme argument l’URI de téléchargement du document XML d’approvisionnement.

```xml
ms-settings:wifi-provisioning?uri={download_uri}
```

Par exemple, le balisage HTML suivant donne un lien pour installer le ou les profils qui se trouvent dans un document hypothétique `http://contoso.com/ProvisioningDoc.xml` .

```html
<a href="ms-settings:wifi-provisioning?uri=http://contoso.com/ProvisioningDoc.xml">Install</a>
```

Votre code XML doit adhérer au schéma de configuration (voir [approvisionnement de comptes](/windows-hardware/drivers/mobilebroadband/account-provisioning)). Votre code XML doit également inclure un ou plusieurs éléments [WLANProfile](./wlan-profileschema-wlanprofile-element.md) . Chaque profil sera affiché dans la boîte de dialogue **Ajouter** décrite ci-après.

quand l’utilisateur clique sur votre lien HTML, le flux de travail d’installation est appelé dans l’application **Paramètres** . votre document XML de provisionnement est téléchargé par l’application **Paramètres** . Une fois téléchargés, des informations sur les profils, la signature et le signataire sont affichées (à condition que le document adhère au schéma).

![application Paramètres](images/install-dialog.png)

le bouton **ajouter** dans la boîte de dialogue de l’application **Paramètres** est activé uniquement si le fichier de configuration est signé et approuvé.

## <a name="in-your-web-page-determine-whether-this-workflow-is-supported"></a>Dans votre page Web, déterminez si ce flux de travail est pris en charge

JavaScript n’a aucun moyen de déterminer la version de build exacte de Windows. toutefois, si votre utilisateur utilise le Microsoft Edge navigateur web, vous pouvez déterminer la version de Edge en inspectant la valeur de l' `User-agent` en-tête HTTP. Si la version est supérieure ou égale à `18.nnnnn` , le flux de travail est pris en charge.

## <a name="related-topics"></a>Rubriques connexes

* [Approvisionnement de comptes](/windows-hardware/drivers/mobilebroadband/account-provisioning)
* [Élément WLANProfile](./wlan-profileschema-wlanprofile-element.md)