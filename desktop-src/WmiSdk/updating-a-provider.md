---
description: Parfois, vous devrez peut-être installer une version plus récente d’un fournisseur sur un système en cours d’exécution.
ms.assetid: 44c4c16a-fd79-483a-81ef-a0f74a2cdf45
ms.tgt_platform: multiple
title: Mise à jour d’un fournisseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4869e6e9f7fbddc3081922f476ca021934065a18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530883"
---
# <a name="updating-a-provider"></a>Mise à jour d’un fournisseur

Parfois, vous devrez peut-être installer une version plus récente d’un fournisseur sur un système en cours d’exécution. Si votre fournisseur est installé en tant que DLL, vous pouvez installer un nouveau fournisseur sans avoir à redémarrer le service, redémarrer l’ordinateur ou affecter une autre application à l’aide de WMI à ce moment-là.

La procédure suivante décrit comment mettre à jour un fournisseur.

**Pour mettre à jour un fournisseur**

1.  Générez le nouveau fournisseur.

    1.  Compilez le nouveau fournisseur avec un nom de DLL et un **CLSID** différents.

        Par exemple, remplacez Myprov.dll par Myprov1.dll et **CLSID \_ MyProProv** par **CLSID \_ MyProv** 1.

    2.  Modifiez le fichier MOF d’inscription du fournisseur pour utiliser le nouveau CLSID (CLSID \_ MyProv1), mais le même nom de fournisseur (« MyProv »).

2.  Installez le nouveau fournisseur.

    1.  Copiez la nouvelle DLL du fournisseur avec le nouveau nom en regard de l’ancien.
    2.  Inscrire automatiquement le nouveau fournisseur.

        Par exemple, utilisez la commande **regsvr32** **myprov1.dll** pour inscrire le nouveau fournisseur.

    3.  Compilez le nouveau MOF d’inscription du fournisseur, remplaçant ainsi l’ancien enregistrement du fournisseur. Jusqu’à ce stade, l’ancien fournisseur était entièrement opérationnel ; désormais, le nouveau fournisseur est entièrement opérationnel.

3.  Supprimez l’ancienne version du fournisseur, si nécessaire.

    1.  Annulez l’inscription de l’ancienne DLL.

        Par exemple, utilisez la commande **regsvr32** **/umyprov.dll** pour annuler l’inscription de l’ancienne dll.

    2.  Marquez l’ancienne DLL à supprimer lors du redémarrage en appelant [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa).

Vous pouvez prendre des mesures similaires pour mettre à niveau un fournisseur local implémenté par le serveur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Développement d’un fournisseur WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Définition des descripteurs de sécurité espace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Sécurisation de votre fournisseur](securing-your-provider.md)
</dt> </dl>

 

 
