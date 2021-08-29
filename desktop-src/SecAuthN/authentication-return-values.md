---
description: Répertorie les valeurs retournées par les fonctions dans les API d’authentification.
ms.assetid: ea519e5c-98b0-4a01-b2cc-e5ff736a5396
title: Valeurs de retour de l’authentification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce618e906bedd1834b0a10ad7569e691034d8071f156c0182e6505fa8444578d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141392"
---
# <a name="authentication-return-values"></a>Valeurs de retour de l’authentification

## <a name="network-provider-values"></a>Valeurs du fournisseur réseau

L' [API du fournisseur réseau](network-provider-api.md) utilise les valeurs définies suivantes.



| Valeur                                                                           | Description                                               |
|---------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Valeurs de retour de sécurité réseau](network-security-return-values.md)<br/> | Retourne les valeurs qu’un fournisseur de réseau peut définir.<br/> |



 

## <a name="smart-card-return-values"></a>Valeurs de retour de carte à puce

Les [fonctions de carte à puce](authentication-functions.md) retournent les valeurs de retour suivantes. Ces valeurs de retour sont définies dans Scarderr. h.

> [!Note]  
> certaines valeurs de retour peuvent avoir la même valeur que les valeurs de retour Windows existantes qui indiquent une condition similaire. Pour plus d’informations sur les codes d’erreur non répertoriés ici, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

 



| Valeur                                                               | Description                                                                                                                                                                                                 |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERREUR \_ de \_ canal rompu<br/> 0x00000109<br/>                | Le client a tenté une opération de carte à distance dans une session à distance, telle qu’une session client s’exécutant sur un serveur Terminal Server, et le système d’exploitation en cours d’utilisation ne prend pas en charge la redirection de carte à puce.<br/> |
| \_ \_ mauvaise recherche E incorrecte \_<br/> 0x80100029<br/>                | Une erreur s’est produite lors de la définition du pointeur d’objet de fichier de carte à puce.<br/>                                                                                                                                 |
| a cicatrice \_ E \_ annulé<br/> 0x80100002<br/>                | L’action a été annulée par une demande [**SCardCancel**](/windows/desktop/api/Winscard/nf-winscard-scardcancel) .<br/>                                                                                                                        |
| \_E impossible de \_ \_ Supprimer<br/> 0x8010000E<br/>            | Le système n’a pas pu supprimer le média de la manière demandée.<br/>                                                                                                                               |
| \_carte E cicatrice \_ \_ non prise en charge<br/> 0x8010001C<br/>        | La carte à puce ne répond pas à la configuration minimale requise pour la prise en charge.<br/>                                                                                                                                   |
| \_certificat E cicatrice \_ \_ non disponible<br/> 0x8010002D<br/> | Impossible d’obtenir le certificat demandé.<br/>                                                                                                                                                 |
| perte de \_ \_ données de comme \_ \_<br/> 0x8010002F<br/>         | Une erreur de communication avec la carte à puce a été détectée. <br/>                                                                                                                                   |
| \_Rép E cicatrice \_ \_ \_ introuvable<br/> 0x80100023<br/>          | Le répertoire spécifié n’existe pas dans la carte à puce.<br/>                                                                                                                                        |
| \_ \_ lecteur dupliqué E en double \_<br/> 0x8010001B<br/>        | Le pilote du [*lecteur*](/windows/desktop/SecGloss/r-gly) n’a pas produit un nom de lecteur unique.<br/>                                                                            |
| \_fichier E cicatrice \_ \_ \_ introuvable<br/> 0x80100024<br/>         | Le fichier spécifié n’existe pas dans la carte à puce.<br/>                                                                                                                                             |
| CREATEORDER d' \_ E \_ ICC \_<br/> 0x80100021<br/>         | L’ordre de création d’objet demandé n’est pas pris en charge.<br/>                                                                                                                                         |
| \_installation ICC E-E \_ \_<br/> 0x80100020<br/>        | Aucun fournisseur principal n’a été trouvé pour la carte à puce.<br/>                                                                                                                                             |
| \_ \_ mémoire tampon insuffisante E \_<br/> 0x80100008<br/>     | Le tampon de données pour les données retournées est trop petit pour les données retournées.<br/>                                                                                                                            |
| \_ \_ ATR E non valide \_<br/> 0x80100015<br/>             | Une [*chaîne ATR*](/windows/desktop/SecGloss/a-gly) obtenue à partir du Registre n’est pas une chaîne ATR valide.<br/>                                                        |
| E- \_ \_ IVT non valides \_<br/> 0x8010002A<br/>             | Le code confidentiel fourni est incorrect.<br/>                                                                                                                                                                   |
| \_ \_ handle E non valide \_<br/> 0x80100003<br/>          | Le handle fourni n’est pas valide.<br/>                                                                                                                                                               |
| \_ \_ paramètre E non valide de cicatrice \_<br/> 0x80100004<br/>       | Un ou plusieurs des paramètres fournis n’ont pas pu être interprétés correctement.<br/>                                                                                                                        |
| \_ \_ cible incorrecte \_ E<br/> 0x80100005<br/>          | Les informations de démarrage du Registre sont manquantes ou non valides.<br/>                                                                                                                                            |
| \_ \_ valeur E non valide \_<br/> 0x80100011<br/>           | Une ou plusieurs des valeurs de paramètre fournies n’ont pas pu être interprétées correctement.<br/>                                                                                                                  |
| E/ \_ r \_ non- \_ accès<br/> 0x80100027<br/>               | L’accès au fichier est refusé.<br/>                                                                                                                                                                    |
| E/ \_ m \_ non- \_ Répertoire<br/> 0x80100025<br/>                  | Le chemin d’accès fourni ne représente pas un répertoire de carte à puce.<br/>                                                                                                                                     |
| E- \_ \_ n \_ fichier non cicatrice<br/> 0x80100026<br/>                 | Le chemin d’accès fourni ne représente pas un fichier de carte à puce.<br/>                                                                                                                                          |
| E. \_ E. \_ pas de \_ conteneur de clé \_<br/> 0x80100030<br/>       | Le conteneur de clé demandé n’existe pas sur la carte à puce.<br/>                                                                                                                                    |
| E de \_ \_ \_ mémoire insuffisante<br/> 0x80100006<br/>               | Mémoire disponible insuffisante pour exécuter cette commande.<br/>                                                                                                                                            |
| E- \_ \_ cache de \_ code confidentiel non \_ cicatrice<br/> 0x80100033<br/>           | Le code confidentiel de la carte à puce ne peut pas être mis en cache.<br/> **Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Ce code d’erreur n’est pas disponible.<br/> <br/>                        |
| \_ \_ lecteur E non \_ \_ disponible<br/> 0x8010002E<br/>   | Aucun lecteur de carte à puce n’est disponible.<br/>                                                                                                                                                               |
| \_E \_ aucun \_ service cicatrice<br/> 0x8010001D<br/>              | Le gestionnaire de [*ressources*](/windows/desktop/SecGloss/r-gly) de carte à puce n’est pas en cours d’exécution.<br/>                                                                |
| pas de \_ \_ carte à \_ puce E a cicatrice<br/> 0x8010000C<br/>            | L’opération nécessite une carte à puce, mais aucune carte à puce n’est actuellement présente dans l’appareil.<br/>                                                                                                               |
| E a cicatrice un \_ \_ \_ tel \_ certificat<br/> 0x8010002C<br/>    | Le certificat demandé n’existe pas.<br/>                                                                                                                                                        |
| E- \_ m \_ non \_ prêt<br/> 0x80100010<br/>               | Le lecteur ou la carte n’est pas prêt à accepter les commandes.<br/>                                                                                                                                              |
| E- \_ E \_ non \_ traité<br/> 0x80100016<br/>          | Une tentative a été effectuée pour terminer une transaction inexistante.<br/>                                                                                                                                            |
| E/ \_ t \_ PCI cicatrice \_ trop \_ petite<br/> 0x80100019<br/>          | La mémoire tampon de réception PCI est trop petite.<br/>                                                                                                                                                            |
| \_ \_ \_ expiration du cache du pin E \_ obsolète<br/> 0x80100032<br/>      | Le cache du code confidentiel de la carte à puce a expiré.<br/> **Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Ce code d’erreur n’est pas disponible.<br/> <br/>                       |
| incompatibilité \_ proto E cicatrice \_ \_<br/> 0x8010000F<br/>          | Les protocoles demandés ne sont pas compatibles avec le protocole en cours d’utilisation avec la carte.<br/>                                                                                                       |
| carte de \_ \_ lecture \_ seule \_ E cicatrice<br/> 0x80100034<br/>         | La carte à puce est en lecture seule et ne peut pas être écrite.<br/> **Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Ce code d’erreur n’est pas disponible.<br/> <br/>       |
| \_lecteur E cicatrice \_ \_ non disponible<br/> 0x80100017<br/>      | Le lecteur spécifié n’est pas disponible pour l’instant.<br/>                                                                                                                                         |
| \_lecteur E cicatrice \_ \_ non pris en charge<br/> 0x8010001A<br/>      | Le pilote du lecteur ne répond pas à la configuration minimale requise pour la prise en charge.<br/>                                                                                                                                |
| \_serveur E cicatrices \_ \_ encombré \_<br/> 0x80100031<br/>        | Le gestionnaire de ressources de carte à puce est trop occupé pour effectuer cette opération.<br/>                                                                                                                          |
| arrêt du \_ service E/m \_ \_<br/> 0x8010001E<br/>         | Le gestionnaire de ressources de carte à puce s’est arrêté.<br/>                                                                                                                                                   |
| VIOLATION de \_ partage E cicatrice \_ \_<br/> 0x8010000B<br/>       | La carte à puce n’est pas accessible en raison d’autres connexions en suspens.<br/>                                                                                                                      |
| \_système E cicatrice \_ \_ annulé<br/> 0x80100012<br/>        | L’action a été annulée par le système, vraisemblablement déconnectée ou arrêtée.<br/>                                                                                                                       |
| \_ \_ délai d’expiration E<br/> 0x8010000A<br/>                  | La valeur du délai d’attente spécifiée par l’utilisateur a expiré.<br/>                                                                                                                                                   |
| E de \_ cicatrice \_ inattendue<br/> 0x8010001F<br/>               | Une erreur de carte inattendue s’est produite.<br/>                                                                                                                                                           |
| \_ \_ carte inconnue E cicatrice \_<br/> 0x8010000D<br/>            | Le nom de carte à puce spécifié n’est pas reconnu.<br/>                                                                                                                                                 |
| \_ \_ lecteur E INconnu \_ cicatrice<br/> 0x80100009<br/>          | Le nom de lecteur spécifié n’est pas reconnu.<br/>                                                                                                                                                     |
| E/ \_ \_ \_ Res MNG inconnues \_<br/> 0x8010002B<br/>        | Un code d’erreur non reconnu a été retourné.<br/>                                                                                                                                                         |
| \_ \_ fonctionnalité E non prise en charge par cicatrices \_<br/> 0x80100022<br/>     | Cette carte à puce ne prend pas en charge la fonctionnalité demandée.<br/>                                                                                                                                          |
| écriture d' \_ E-E \_ \_ trop \_ nombreuses<br/> 0x80100028<br/>         | Une tentative a été effectuée pour écrire plus de données que dans l’objet cible.<br/>                                                                                                                      |
| \_erreur comm. F. \_ \_<br/> 0x80100013<br/>              | Une erreur de communication interne a été détectée.<br/>                                                                                                                                              |
| \_erreur interne de F a cicatrice \_ \_<br/> 0x80100001<br/>          | Une vérification de cohérence interne a échoué.<br/>                                                                                                                                                            |
| \_ \_ erreur inconnue en F \_<br/> 0x80100014<br/>           | Une erreur interne a été détectée, mais la source est inconnue.<br/>                                                                                                                                  |
| le F a cicatrice un temps d’attente \_ \_ \_ trop \_ long<br/> 0x80100007<br/>        | Un minuteur de cohérence interne a expiré.<br/>                                                                                                                                                       |
| arrêt de \_ P a cicatrice \_<br/> 0x80100018<br/>                 | L’opération a été abandonnée pour permettre à l’application serveur de se fermer.<br/>                                                                                                                          |
| succès des \_ S \_<br/>                                        | Aucune erreur n’a été rencontrée.<br/>                                                                                                                                                                        |
| a CICATRICEd \_ W \_ annulé \_ par l' \_ utilisateur<br/> 0x8010006E<br/>      | L’action a été annulée par l’utilisateur.<br/>                                                                                                                                                             |
| Impossible de \_ \_ trouver un élément de cache de W avec \_ \_ cicatrices \_<br/> 0x80100070<br/>  | L’élément demandé est introuvable dans le cache.<br/>                                                                                                                                              |
| élément de \_ \_ cache W en trop \_ \_ obsolète<br/> 0x80100071<br/>       | L’élément de cache demandé est trop ancien et a été supprimé du cache.<br/>                                                                                                                              |
| élément de \_ \_ cache W \_ \_ trop \_ volumineux<br/> 0x80100072<br/>    | Le nouvel élément de cache dépasse la taille maximale par élément définie pour le cache.<br/>                                                                                                                      |
| \_carte avec cicatrices \_ \_ non \_ authentifiée<br/> 0x8010006F<br/> | Aucun code PIN n’a été présenté à la carte à puce.<br/>                                                                                                                                                          |
| e/ \_ s IVT a cicatrices \_ \_ bloquées<br/> 0x8010006C<br/>             | Impossible d’accéder à la carte, car le nombre maximal de tentatives de saisie du code confidentiel a été atteint.<br/>                                                                                                   |
| a CICATRICEd \_ W \_ EOF<br/> 0x8010006D<br/>                      | La fin du fichier de carte à puce a été atteinte.<br/>                                                                                                                                                 |
| \_carte avec une \_ carte supprimée \_<br/> 0x80100069<br/>            | La carte à puce a été supprimée, de sorte que les communications supplémentaires ne sont pas possibles.<br/>                                                                                                                       |
| carte de \_ \_ réinitialisation avec cicatrices \_<br/> 0x80100068<br/>              | La carte à puce a été réinitialisée.<br/>                                                                                                                                                                        |
| VIOLATION de \_ sécurité de W a cicatrice \_ \_<br/> 0x8010006A<br/>      | L’accès a été refusé en raison d’une violation de sécurité.<br/>                                                                                                                                               |
| \_ \_ carte inpowered W sans alimentation \_<br/> 0x80100067<br/>          | L’alimentation a été retirée de la carte à puce, de sorte que les communications supplémentaires ne sont pas possibles.<br/>                                                                                                       |
| carte sans \_ \_ réponse avec cicatrice \_<br/> 0x80100066<br/>       | La carte à puce ne répond pas à une réinitialisation.<br/>                                                                                                                                                     |
| \_ \_ carte non prise en charge avec \_ cicatrice<br/> 0x80100065<br/>        | Le lecteur ne peut pas communiquer avec la carte, en raison de conflits de configuration de chaîne ATR.<br/>                                                                                                          |
| \_mauvaises e- \_ bonnes \_ IVT<br/> 0x8010006B<br/>               | Impossible d’accéder à la carte en raison de la présentation d’un PIN incorrect.<br/>                                                                                                                                 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Codes d’erreur système](/windows/desktop/Debug/system-error-codes)
</dt> </dl>

 

