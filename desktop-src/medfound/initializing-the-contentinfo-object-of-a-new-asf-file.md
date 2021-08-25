---
description: Initialisation de l’objet ContentInfo d’un nouveau fichier ASF
ms.assetid: a4f6c90e-1b38-4c70-8bc5-e2e16af3d87a
title: Initialisation de l’objet ContentInfo d’un nouveau fichier ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf0180eb4e9369447355a9a4cd607f630bfb3664108ad77d6d008c281f92fdf1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114249"
---
# <a name="initializing-the-contentinfo-object-of-a-new-asf-file"></a>Initialisation de l’objet ContentInfo d’un nouveau fichier ASF

Après avoir créé un objet ContentInfo vide en appelant la fonction [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) , l’application doit appeler [**IMFASFContentInfo :: SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) pour fournir le profil d’encodage. Pour plus d’informations sur la création d’un profil, consultez [création d’un profil ASF](creating-an-asf-profile.md).

Pour que les informations puissent être lues à partir du profil, la méthode **SetProfile** doit valider l’objet de profil spécifié en vérifiant les identificateurs de flux ou les types de média. Si le profil réussit la validation, plusieurs objets d’en-tête sont générés, tels que l’objet de propriétés de fichier, l’objet de propriétés de débit binaire, l’objet de propriétés de flux et l’objet d’exclusion mutuelle.

**SetProfile** calcule et définit les valeurs recommandées pour certaines propriétés, telles que la valeur de préroll. Si ce n’est pas déjà fait, la valeur de préroll recommandée en millisecondes dépend de la fenêtre de mémoire tampon maximale du compartiment avec fuite spécifié pour les flux dans le profil. De même, les tailles de paquets de données minimale et maximale sont également définies. Les valeurs recommandées peuvent remplacer les tailles de paquets définies sur le profil par le biais d’attributs.

Étant donné que le fichier est en cours de création, le fichier est catégorisé comme type de diffusion, ce qui est indiqué par le champ Flags de l’objet de propriétés de fichier. Certaines valeurs inconnues, telles que le nombre de paquets de données, la durée de lecture et la durée d’envoi, sont définies sur zéro. Ces valeurs sont représentées par les attributs **MF \_ PD \_ ASF \_ xxx** et doivent être mises à jour par l’application une fois la création du fichier terminée.

L’objet de profil spécifié remplace tout profil existant associé à l’objet ContentInfo, supprime les objets d’en-tête référencés et réinitialise les propriétés globales du fichier, telles que la taille des paquets de données et du préroll.

La méthode **SetProfile** crée également l’objet de données qui représente l’objet de données ASF. Si vous réutilisez un objet ContentInfo qui contient des informations sur les paquets de données, **SetProfile** échoue et retourne l' \_ erreur MF E \_ déjà \_ initialisée, indiquant qu’il est déjà associé à un objet de données ASF existant. Par défaut, pour un nouvel objet ContentInfo, le nombre de paquets de données est défini sur zéro et la taille de l’objet de données est définie sur 50 octets. Si vous utilisez le multiplexeur pour générer des paquets de données, le multiplexeur met à jour l’objet ContentInfo pour refléter les nouvelles valeurs, telles que le nombre de paquets de données. Pour plus d’informations sur la génération de paquets de données, consultez [génération de nouveaux paquets de données ASF](generating-new-asf-data-packets.md).

Une fois que tous les objets d’en-tête sont ajoutés à l’objet d’en-tête ASF final, la taille totale de l’en-tête peut être récupérée en appelant [**IMFASFContentInfo :: GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize). Cette taille comprend la taille initiale de l’objet de données.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition des propriétés dans l’objet ContentInfo](setting-properties-in-the-contentinfo-object.md)
</dt> <dt>

[Écriture d’un objet d’en-tête ASF pour un nouveau fichier](writing-an-asf-header-object-for-a-new-file.md)
</dt> </dl>

 

 



