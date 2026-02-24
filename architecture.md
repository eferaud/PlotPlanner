Le projet doit respecter la Clean Architecture, en s'appuyant sur les cas d'utilisations déinit dans use-cases.md

Package à respecter : 
fr.feraud.plotplanener.domain.model
fr.feraud.plotplanener.domain.service
fr.feraud.plotplanener.domain.event

fr.feraud.plotplanener.application.usecase
fr.feraud.plotplanener.application.port.in
fr.feraud.plotplanener.application.port.out
fr.feraud.plotplanener.application.dto
fr.feraud.plotplanener.application.mapper

fr.feraud.plotplanener.adapters.in.web
fr.feraud.plotplanener.adapters.out.persistence

fr.feraud.plotplanener.infrastructure.config
fr.feraud.plotplanener.infrastructure.security
fr.feraud.plotplanener.infrastructure.persistence (config de la DB et datasource)
fr.feraud.plotplanener.infrastructure.bootstrap (le Main)


Dépendances à respecter : 
domain ne doit dependre de rien
application → domain
adapters → application
adapters → domain (autorisé)
infrastructure → adapters
infrastructure → application
infrastructure → domain
