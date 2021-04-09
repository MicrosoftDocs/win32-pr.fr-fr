---
description: CertMgr
ms.assetid: c9b68a81-c4f7-4754-9b47-c83f3679f0e3
title: CertMgr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b0e248aef1f726b16d8f17098cfc9642393b963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115322"
---
# <a name="certmgr"></a>CertMgr

Les outils CertMgr remplacent DumpCert. Il comprend de nouvelles fonctionnalités pour la gestion des [*certificats*](../secgloss/c-gly.md), des [*listes*](../secgloss/c-gly.md) de certificats de confiance (CTL) et des [*listes de révocation de certificats*](../secgloss/c-gly.md) (CRL). L’outil est installé dans le \\ dossier bin du chemin d’installation du kit de développement logiciel (SDK) Microsoft Windows.

CertMgr est disponible dans le cadre de la SDK Windows, que vous pouvez télécharger à partir de <https://go.microsoft.com/fwlink/p/?linkid=84091> .

CertMgr exécute l’une des quatre fonctions en fonction de l’action indiquée dans la commande.

**Certmgr** \[ **-Ajouter** \| **-del** \| **-put** \] \[  \] Options \[ **-s** \[ **-r** *RegistryLocation* \] \] *SourceName* \[ **-s** \[ **-r** *RegistryLocation* \] \] \[ *DestinationName*\]

Le tableau suivant indique les actions de base de l’outil CertMgr.



| Indicateur d’action | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| aucun        | Affiche les certificats, les listes de révocation de certificats ou les CTL. sans indicateur d’action (pour afficher uniquement), *SourceName* est le nom du magasin de certificats ou du fichier contenant les éléments à afficher. Le magasin peut être un magasin [*sérialisé*](../secgloss/s-gly.md) (StoreFile) ou un magasin système. Par défaut, CertMgr affiche tous les certificats, listes de certificats de confiance ou listes de révocation de certificats dans le magasin de certificats ou le fichier. *DestinationName* n’est pas utilisé pour l’affichage.<br/>                                                                                                                                                                                                                                                                                                                                  |
| -Ajouter        | Copie les certificats, listes de certificats de confiance et listes de révocation de certificats dans un magasin de certificats. Lors de l’utilisation **de-Add**, *SourceName* est le magasin de certificats source qui contient les certificats, listes de certificats de confiance et listes de révocation de certificats existants. *DestinationName* est le magasin de certificats de destination auquel les certificats, listes de certificats de confiance et listes de révocation de certificats seront ajoutés. Le magasin de destination sera enregistré en tant que magasin [*sérialisé*](../secgloss/s-gly.md) , sauf si l’option **-7** est utilisée, ce qui permet d’enregistrer le magasin sous la forme d’un fichier [*PKCS*](../secgloss/p-gly.md) \# 7. Notez que l’option **-7** ne peut pas être utilisée lorsque le magasin de destination est un magasin système.<br/>                                                                                                                          |
| -del        | Supprime des certificats, des listes CTL et des listes de révocation de certificats d’un magasin de certificats. Lors de l’utilisation **de-del**, *SourceName* est le magasin de certificats source qui contient les certificats, listes de certificats de confiance et listes de révocation de certificats existants. *DestinationName* est le magasin de certificats de destination qui contient des copies des certificats, listes de certificats de confiance et listes de révocation de certificats restants après la suppression des éléments spécifiés. Si *DestinationName* n’est pas spécifié, *SourceName* est également utilisé comme magasin de destination (il sera modifié). Le magasin de destination sera enregistré en tant que magasin [*sérialisé*](../secgloss/s-gly.md) , sauf si l’option **-7** est utilisée, ce qui permet d’enregistrer le magasin sous la forme d’un \# fichier PKCS 7. Notez que l’option **-7** ne peut pas être utilisée lorsque le magasin de destination est un magasin système.<br/> |
| -put        | Enregistre dans un fichier un certificat encodé [*X. 509*](../secgloss/x-gly.md) , une liste CTL ou une liste de révocation de certificats. Quand vous utilisez **-put**, *SourceName* est le magasin de certificats source qui contient les certificats, listes de certificats de confiance et listes de révocation de certificats existants. *DestinationName* est le nom d’un fichier dans lequel un certificat, une liste CTL et une liste de révocation de certificats codés [*X. 509*](../secgloss/x-gly.md) seront enregistrés. Si l’option **-7** est utilisée, le fichier est enregistré sous la forme d’un \# fichier PKCS 7.<br/>                                                                                                                                                                                                                                                                                             |



 

## <a name="options"></a>Options

Les options suivantes s’appliquent à toutes les fonctions CertMgr, sauf indication contraire.



| Option                     | Indicateur d’action                                 | Description                                                                                                                                                                                                                                        |
|----------------------------|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-v**                     | aucun (affichage uniquement)                         | Mode documenté. Affiche des informations détaillées sur les certificats, les listes CTL et les listes de révocation de certificats. La valeur par défaut consiste à afficher de brèves informations.                                                                                                                       |
| **-c**                     | all                                         | Utilisez uniquement des certificats.                                                                                                                                                                                                                             |
| **-CTL**                   | all                                         | Utilisez uniquement des listes CTL.                                                                                                                                                                                                                                     |
| **-CRL**                   | all                                         | Utilisez uniquement des listes de révocation de certificats.                                                                                                                                                                                                                                     |
| **-tout**                   | **-Add-del**<br/> **-put**<br/> | Ajoute toutes les entrées du type choisi.                                                                                                                                                                                                               |
| **-e** *encodingType*      | all                                         | [*Type d’encodage*](../secgloss/e-gly.md)de certificat.                                                                                                                                             |
| **-y** *storeProviderType* | all                                         | Type de fournisseur de magasin.                                                                                                                                                                                                                               |
| **7**                     | **-Add-del**<br/> **-put**<br/> | Enregistre le magasin de destination en tant que \# fichier PKCS 7.                                                                                                                                                                                                    |
| **-f** *dwFlags*           | all                                         | Enregistrer l’indicateur d’ouverture. Il s’agit du paramètre *dwFlags* passé à [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore). La valeur par défaut est CERT \_ System \_ Store \_ Current \_ User. Significatif uniquement si **-y** est défini. Pour plus d’informations, consultez **CertOpenStore**.         |
| **-n** *commonNameString*  | **-Add-del**<br/> **-put**<br/> | Nom commun du certificat. Peut être utilisé uniquement avec des certificats.                                                                                                                                                                                |
| **-SHA1** *sha1Hash*       | **-Add-del**<br/> **-put**<br/> | Hachage SHA1 du certificat, de la liste de certificats de confiance ou de la liste de révocation de certificats à copier, supprimer ou enregistrer.                                                                                                                                                                         |
| **-s**                     | all                                         | Indique que le magasin est un magasin système.                                                                                                                                                                                                        |
| **-r** *registryLocation*  | all                                         | Emplacement du Registre du magasin de certificats système. Significatif uniquement lorsque **-s** est défini. Doit avoir la valeur *CurrentUser* (clé de Registre HKEY \_ Current \_ User) ou *LOCALMACHINE* (clé de Registre HKEY \_ local \_ machine). *CurrentUser* est la valeur par défaut. |
| **-?**                     | all                                         | Affiche toutes les options.                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Notes

CertMgr est pris en charge uniquement dans Internet Explorer 4,0 ou version ultérieure.

CertMgr peut copier, supprimer ou enregistrer un ou plusieurs certificats, listes de certificats de confiance ou listes de révocation de certificats. Si plusieurs éléments se trouvent dans l’une de ces catégories, l’utilisateur dispose de trois options :

-   Utilisez l’option **-All** pour copier, supprimer ou enregistrer tous les éléments de la catégorie indiquée.
-   Utilisez les options **-n** et **-SHA1** pour identifier de manière unique l’élément à copier, supprimer ou enregistrer.
-   Si **-All**, ou **-n** et **-SHA1** ne sont pas indiqués, certmgr invite l’utilisateur à fournir une liste d’éléments à copier, supprimer ou enregistrer. L’utilisateur répond en entrant l’index de l’élément à copier, supprimer ou enregistrer.

Les actions de CertMgr utilisent de légères variations de la syntaxe et des options. La syntaxe et les options propres à une action doivent être utilisées.

CertMgr fonctionne avec deux types de magasins de certificats : StoreFile et magasin système. Un StoreFile peut être l’un des types de fichiers suivants :

-   Un fichier de certificat/liste de certificats de confiance/CRL encodé (peut être encodé en base 64)
-   Un \# fichier PKCS 7
-   Un document signé
-   StoreFile sérialisé

Il n’est pas nécessaire de spécifier le type de StoreFile. CertMgr peut déterminer le type de StoreFile et prendre les mesures appropriées.

Un magasin système est un magasin de certificats situé normalement dans le Registre sous **CurrentUser**. L’utilisateur peut se référer à un magasin système en fournissant son nom uniquement. Il n’est pas nécessaire de spécifier le type de fournisseur de magasin de certificats. Selon le type de StoreFile ou du magasin système, CertMgr choisit le type de fournisseur de stockage correspondant.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de CertMgr](using-certmgr.md)
</dt> </dl>

 

 
